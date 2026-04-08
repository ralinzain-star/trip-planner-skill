# Crowd Avoidance Intelligence — Design Spec

**Date:** 2026-04-06
**Status:** Approved
**Scope:** Add crowd/busyness intelligence to trip-planner-skill.md

## Overview

Add a three-layer crowd avoidance system that uses Google Maps Popular Times data, travel blog insights, and cultural knowledge to optimize itineraries for minimal crowds.

## Changes by Phase

### Phase 4 (Deep Research) — New item #15: Crowd Intelligence

For each selected attraction, research busyness patterns and store as a `crowd` object on the POI.

**Search strategy:**
- `"{attraction}" popular times`
- `"{attraction}" best time to visit avoid crowds`
- `"{attraction}" 混雑 / 人多 / 避開人潮` (destination language)
- `"{destination} public holidays {year}"` for holiday calendar
- `"{destination} festivals {month} {year}"` for event-driven surges

**Data stored per POI (`crowd` field in trip.json):**
```json
{
  "peak_hours": ["10:00-14:00"],
  "off_peak_hours": ["07:00-09:00", "16:00-18:00"],
  "best_visit_window": "08:00-09:30",
  "peak_days": ["sat", "sun", "holidays"],
  "off_peak_days": ["tue", "wed", "thu"],
  "wait_time_peak": "15-20 min queues for photos",
  "wait_time_offpeak": "Almost no queues",
  "crowd_level": "high | medium | low",
  "tips": ["Tue-Thu least crowded", "Afternoon backlit, go in morning"],
  "seasonal_note": "Cherry blossom season (Mar-Apr) 2-3x normal crowds",
  "source": "Google Maps Popular Times + travel blogs"
}
```

**Fallback rules when Popular Times data unavailable:**
- Temples/shrines: weekends + morning = peak
- Markets: weekends + midday = peak
- Museums: closed-day + 1 = compensatory peak
- Nature/outdoor: weather-dependent, weekends peak
- Shopping streets: Fri evening + weekends = peak

### Phase 3 Step 3b (Route Plan) — Add crowd column

Route plan table gains a 4th column:

```
| Time | Activity | Transit | Crowd |
|------|----------|---------|-------|
| 08:00 | Gamcheon Village | Bus 25min | [LOW] Best before 09:30 |
| 14:00 | Haedong Yonggungsa | Bus 50min | [HIGH→MED] Crowds thin after 15:00 |
```

Labels: `[LOW]` `[MED]` `[HIGH]` — with one-line context.

**Intra-day ordering rule:**
1. Hot attractions → schedule during their off_peak_hours
2. Cool attractions → fill remaining slots (flexible)
3. If two hot attractions' off_peak windows conflict → split across days
4. Restaurants: avoid 12:00-13:00 lunch rush, 18:00-19:30 dinner rush
   → suggest 11:30/13:30 lunch, 17:30/20:00 dinner

### Phase 3 Step 3g (new) — Crowd-Aware Cross-Day Optimization

Runs AFTER Step 3f (geographic optimization). A second optimization pass.

**Algorithm:**
1. Identify which travel dates are weekends/local holidays
2. Attractions with `peak_days: ["sat","sun"]` → move to weekdays
3. Weekends/holidays → assign nature, suburban, hiking (crowd-dispersed activities)
4. If a local festival falls during the trip → ask user: avoid or embrace?

**Output format:**
```
Crowd Optimization Analysis:

✅ 4/1 (Tue) Gamcheon Village — weekday, low crowd expected
⚠️ 4/5 (Sat) Seomyeon Shopping — Saturday peak, high crowds
  💡 Swap with 4/3 (Thu) Taejongdae — outdoor spot, weekend impact is lower

🎌 4/3 is Arbor Day (KR public holiday):
  → City attractions will be crowded
  → Option A: Swap to suburban itinerary
  → Option B: Go to Yeouido Cherry Blossom Festival (crowded but worth it) — your call?
```

### Phase 5 (HTML) — Visual crowd indicators

**Calendar tab events:**
- Small badge top-right: green `LOW` / amber `MED` / red `HIGH`
- Tooltip on hover/tap: "Best before 09:30, peak at 10:00-14:00"

**Attractions tab POI cards:**
- "Best time" badge: e.g., `Best: 08:00-09:30`
- "Avoid" badge: e.g., `Avoid: 10:00-14:00 weekends`

**POI detail modal — new "Crowd" section:**
- Visual bar chart (like Google Maps Popular Times) showing busyness by hour
- Peak/off-peak labels
- Tips list

**Today Dashboard — crowd alert:**
- If next event is during its peak_hours → show warning card:
  "{Attraction} is crowded right now. Consider {nearby cafe} for 1 hour first."

### trip.json schema addition

`crowd` field added to each POI object (see data structure above).

## Files Modified

- `/Users/harmony/Documents/GitHub/trip-planner-skill/main/trip-planner-skill.md` — all changes in this single file

## Insertion Points

1. **Phase 3 Step 3b table format** (line ~635): add Crowd column to route table
2. **After Phase 3 Step 3f** (line ~780): new Step 3g for cross-day crowd optimization
3. **Phase 3 Confirmation Gate** (line ~893): add crowd optimization to confirmation text
4. **Phase 4 Research Checklist item 5** (line ~943): expand with crowd research
5. **New Phase 4 item #15** (after item 14): dedicated crowd intelligence research
6. **Phase 5 Today Dashboard during-trip mode** (line ~1448): add crowd alert
7. **Phase 5 Interactive Features** (line ~2274): add crowd indicators to calendar/POI specs
8. **Phase 5 POI detail modal** (line ~2319): add crowd section
