# Playful Geometric

> "Stable Grid, Wild Decoration" — clean readable content with energetic surrounding elements. Memphis Group aesthetics modernized for digital.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FFFDF5` | Warm cream |
| Foreground | `#1E293B` | Slate 800 |
| Muted BG | `#F1F5F9` | Slate 100 |
| Muted FG | `#64748B` | Slate 500 |
| Accent | `#8B5CF6` | Vivid violet (primary) |
| Secondary | `#F472B6` | Hot pink |
| Tertiary | `#FBBF24` | Amber/yellow |
| Quaternary | `#34D399` | Emerald/mint |
| Border | `#E2E8F0` | Slate 200 |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Outfit** | 700-800 | Geometric sans, rounded |
| Body | **Plus Jakarta Sans** | 400-500 | Geometric-humanist hybrid |

- Scale ratio: 1.25 (Major Third)
- Hero: `text-4xl` to `text-6xl`

## Border Radius

- Small: 8px | Medium: 16px | Large: 24px | Full: 9999px
- Buttons: `rounded-full` (pill)
- Cards: `rounded-xl` (16px)
- Border width: 2px standard

## Shadows (Hard "Pop" — No Blur)

```css
/* Default */
box-shadow: 4px 4px 0px 0px #1E293B;

/* Hover (lift) */
box-shadow: 6px 6px 0px 0px #1E293B;

/* Active (press) */
box-shadow: 2px 2px 0px 0px #1E293B;
```

No blur on any shadow — sticker/cut-paper aesthetic.

## Spacing

- Section padding: `py-24` (96px)
- Card padding: `p-6` to `p-8` (24-32px)
- Container: `max-w-6xl`
- Grid: 12-column (6/6, 4/4/4)

## Component Patterns

### Buttons ("Candy Button")
- Accent violet bg, white text, `font-bold`
- `rounded-full`, `border-2 border-[#1E293B]`
- Hard shadow: `4px 4px 0px #1E293B`
- Hover: `translate(-2px,-2px)` + 6px shadow (lift)
- Active: `translate(2px,2px)` + 2px shadow (press)
- Secondary: transparent, fills with tertiary yellow on hover

### Cards ("Sticker")
- White bg, `border-2 border-[#1E293B]`, `rounded-xl`
- Shadow: `8px 8px 0px #E2E8F0` (pink on featured cards)
- Hover: `rotate(-1deg)`, `scale(1.02)`
- Featured card: scaled 1.1x with colored shadow

### Inputs
- White bg, `border-2 border-[#CBD5E1]`, `rounded-lg`
- Focus: accent border + `4px` hard shadow
- Labels: bold, uppercase, wide tracking

## Animation

- Easing: `cubic-bezier(0.34, 1.56, 0.64, 1)` — bounce/overshoot
- Duration: 300ms
- Entrance: pop-in (scale 0 → 1 with bounce)
- Marquee: infinite scroll
- Wiggle: 0deg → 3deg → -3deg → 0deg on hover

## Signature Elements

1. **Primitive shapes** as backgrounds — circles, triangles, squares, pills, squiggles
2. **Pattern fills** — polka dots, grids, diagonal stripes
3. **Hard shadows** (no blur) — sticker/cut-paper look
4. **Bouncy animations** with overshoot easing
5. **Confetti SVG shapes** behind content sections
6. **Rotated elements** — slight tilt for playfulness
7. **"MOST POPULAR" badge** — 15deg rotated star
8. **Icons enclosed in colored shapes** (stroke 2.5px, bold)

## Anti-Patterns

- No subtle/muted aesthetics
- No standard drop shadows (hard offset only)
- No serious/corporate tone
- No monochrome sections
- No thin borders (2px minimum)
