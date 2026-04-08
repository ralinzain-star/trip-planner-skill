### trip.json Complete Schema (MANDATORY)

`data/trip.json` is the data backbone of the entire app. Below is the full top-level structure; every field is required unless explicitly marked optional:

```json
{
  "destination": "釜山→阿蘇→福岡",
  "tagline": {
    "zh": "在櫻花盛開的季節，從海邊城市走進火山秘境",
    "en": "From coastal city to volcanic wonders, under cherry blossoms",
    "ko": "벚꽃이 만개하는 계절, 해변 도시에서 화산 비경으로",
    "ja": "桜満開の季節、海辺の街から火山の秘境へ"
  },
  "startDate": "2026-03-30",
  "endDate": "2026-04-12",
  "currency": {
    "home": "TWD",
    "rates": { "KRW": 42, "JPY": 5, "USD": 0.031 }
  },
  "entryRequirements": [ ... ],
  "flightIntel": { ... },
  "holidays": { ... },
  "pois": [ ... ],
  "schedule": [ ... ],
  "budget": { "items": [ ... ] },
  "checklist": [ ... ]
}
```

#### `entryRequirements[]` -- Entry Form Prefill Tasks

One entry per visited country, containing any online entry forms the user must complete:

```json
"entryRequirements": [
  {
    "country": "KR",
    "name": { "zh": "🇰🇷 韓國", "en": "🇰🇷 Korea", "ko": "🇰🇷 한국", "ja": "🇰🇷 韓国" },
    "items": [
      {
        "task": { "zh": "電子入境卡 e-Arrival Card", "en": "e-Arrival Card", "ko": "전자입국카드", "ja": "電子入国カード" },
        "url": "https://www.e-arrivalcard.go.kr/",
        "deadline": { "zh": "3/27 起可填（抵達前3天）", "en": "From 3/27 (3 days before arrival)", ... },
        "status": "pending"
      }
    ]
  },
  {
    "country": "JP",
    "name": { "zh": "🇯🇵 日本", "en": "🇯🇵 Japan", ... },
    "items": [
      {
        "task": { "zh": "Visit Japan Web", "en": "Visit Japan Web", ... },
        "url": "https://www.vjw.digital.go.jp/",
        "deadline": { "zh": "出發前隨時可填", "en": "Fill anytime before departure", ... },
        "status": "pending"
      }
    ]
  }
]
```

- `status`: `"pending"` | `"done"` -- user can check items in the Today overlay and Checklist tab
- Only include **items that require an online form** (e.g., e-Arrival Card, Visit Japan Web, ESTA). Put generic reminders in the checklist.

#### `flightIntel` -- Flight Price History Analysis

Used for flight price evaluation in the Booking tab and flight info in the Today overlay:

```json
"flightIntel": {
  "route": "TPE ↔ PUS/FUK",
  "userPrice": 19600,
  "booked": true,
  "monthlyPrices": [
    { "month": "4月", "label": "Apr", "avg": 14500, "note": "淡季尾" },
    { "month": "5月", "label": "May", "avg": 15200, "note": "" },
    ...
  ],
  "range": { "low": 12000, "high": 28000, "avg": 21750 }
}
```

- `userPrice`: the price the user actually paid (in home currency, e.g., TWD)
- `booked`: whether the flight is already purchased
- `monthlyPrices`: 12 months of historical averages for the price trend chart
- `range`: 12-month low/high/avg used to compute the verdict (green below avg / yellow near avg / red above avg)
- `renderFlightIntel()` renders the inline verdict badge on the Booking tab flight card

#### `holidays` -- Holiday Data

Holidays for the user's home country, used for the Booking tab holiday calendar and PTO-bridging tips:

```json
"holidays": {
  "country": "TW",
  "countryName": "台灣",
  "items": [
    {
      "date": "2026-04-03",
      "name": "清明節",
      "days": "4/2–4/5 四天連假",
      "tip": "請0天放4天",
      "active": true
    },
    { "date": "2026-05-01", "name": "勞動節", "days": "5/1（五）", "tip": "請0天放3天" },
    ...
  ]
}
```

- `active: true` marks holidays overlapping the trip dates
- `tip` provides PTO-bridging guidance (e.g., "Take X days off to get Y days total")

#### `pois[]` -- POI (Attractions) Data

```json
{
  "id": "b1",
  "name": "龍頭山公園+釜山塔",
  "name_en": "Yongdusan Park+Busan Tower",
  "name_ko": "용두산공원/부산타워",
  "name_ja": "龍頭山公園+釜山タワー",
  "nameLocal": "용두산공원/부산타워",
  "city": "busan",
  "cat": "attraction",
  "lat": 35.1008, "lng": 129.0325,
  "price_krw": 7200, "price_twd": 173,
  "hours": "09:00–22:00",
  "desc": "⭐必去 · 3/31 09:30-10:30 · ₩7,200",
  "addr": "南浦洞"
}
```

- `city`: lowercase city key (`busan`, `aso`, `fukuoka`) -- used for filters and map marker grouping
- `cat`: `attraction` | `food` | `cafe` | `shopping` | `transport` | `work` | `hotel` | `other`
- `price_krw`/`price_jpy`: local currency price; `price_twd`: converted home-currency price
- `nameLocal`: local-language name used in the destination country (for Google Maps search)

#### `schedule[]` -- Daily Itinerary

```json
{
  "date": "2026-03-31",
  "city": "釜山",
  "events": [
    {
      "sh": 10, "eh": 12,
      "name": "釜山電影體驗博物館",
      "name_en": "Busan Cinema Experience Museum",
      "name_ko": "부산영화체험박물관",
      "name_ja": "釜山映画体験博物館",
      "cat": "attraction",
      "note": "₩10,000 · 龍頭山旁 · 室內",
      "note_en": "₩10,000 · Next to Yongdusan · Indoor",
      "note_ko": "₩10,000 · 용두산 옆 · 실내",
      "note_ja": "₩10,000 · 龍頭山隣 · 室内",
      "restaurant": "국제시장 돼지국밥",
      "map": "https://www.google.com/maps/search/?api=1&query=...",
      "reservation": false,
      "booking_url": "https://...",
      "booking_note": "Reservations open 2 weeks before"
    }
  ]
}
```

- `sh`/`eh`: start/end time (decimal hours, e.g., 10.5 = 10:30) -- use the day's city local timezone
- `city`: city name in the user's display language for schedule rendering (translate via the `SCHEDULE_CITY_I18N` mapping)
- `restaurant`/`map`/`reservation`: required for food events
- `booking_url`/`booking_note`: optional for items that require reservations

#### `budget.items[]` -- Budget Line Items

```json
{
  "name": "✈️ 機票來回 IT606+IT241",
  "name_en": "✈️ Round-trip Flights IT606+IT241",
  "name_ko": "✈️ 왕복 항공권 IT606+IT241",
  "name_ja": "✈️ 往復航空券 IT606+IT241",
  "city": "busan",
  "cat": "transport",
  "cost_twd": 19600,
  "checked": false
}
```

- `cost_twd`: denominated in the user's home currency
- `checked`: default `false`; when checked, reduce opacity + add a strikethrough; totals update in real time

#### `checklist[]` -- Pre-trip Checklist (Full i18n)

```json
[
  {
    "title": { "zh": "證件 & 簽證", "en": "Documents & Visa", "ko": "서류 & 비자", "ja": "書類 & ビザ" },
    "items": [
      { "zh": "護照有效期 6個月以上", "en": "Passport valid 6+ months", "ko": "여권 유효기간 6개월 이상", "ja": "パスポート有効期限6ヶ月以上" },
      ...
    ]
  },
  ...
]
```

- Each group has a `title` (i18n object) and `items` (array of i18n objects)
- Default groups: Documents & Visa, Finance & Exchange, Must-have Apps (Korea), Must-have Apps (Japan), Internet & Power, Luggage & Clothing
