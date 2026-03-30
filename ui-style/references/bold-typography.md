# Bold Typography

> "Poster design translated to web" — typography is the primary visual language, not decoration. Confident. Editorial. Deliberate.

## Color Palette (Dark Mode)

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#0A0A0A` | Near-black surface |
| Foreground | `#FAFAFA` | Warm white text |
| Muted BG | `#1A1A1A` | Subtle elevation |
| Muted FG | `#737373` | Secondary text |
| Accent | `#FF3D00` | Vermillion/red-orange |
| Border | `#262626` | Barely-visible dividers |
| Card | `#0F0F0F` | Slight elevation |

Restrained: black, white, and one vermillion accent.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headlines | **Inter Tight** | 700-900 | Condensed impact |
| Pull quotes | **Playfair Display** | 400-700 | Serif contrast |
| Labels/Stats | **JetBrains Mono** | 400-500 | Technical data |

- Hero scale: extreme — 6:1+ ratio between H1 and body minimum
- Display: `text-8xl` to `text-9xl` (128-160px)
- Labels: uppercase, `tracking-wider`
- Body: `text-base` to `text-lg`

## Border Radius

**`0px` on ALL elements.** Sharp corners only — no exceptions.

## Shadows

**None.** Depth via layered typography, accent underlines, full-width dividers.

## Borders

- Full-width `border-b border-[#262626]` dividers
- Minimal use — structural only

## Spacing

- Section padding: `py-24` to `py-40`
- Card padding: `p-8` to `p-12`
- Generous negative space everywhere
- Container: `max-w-6xl`

## Component Patterns

### Buttons
- Accent bg (`#FF3D00`), dark text
- Sharp corners, no shadow
- Hover: brightness increase
- Uppercase, bold

### Cards
- `#0F0F0F` bg, `border border-[#262626]`
- Hover: accent underline appears on title
- No shadows, no lift

### Links / Interactions
- Accent underlines as primary affordance
- Hover reveals vermillion color
- Underline slides in from left

## Animation

- 150ms micro-interactions: `cubic-bezier(0.25, 0, 0, 1)`
- 200ms standard interactions
- 500ms image hover transitions
- Fast-out, crisp stop — no bounce

## Signature Elements

1. **Extreme typography scale** — 6:1+ ratio minimum between sizes
2. **Accent underlines** as primary interaction affordance
3. **Vermillion accent** (`#FF3D00`) — the only color
4. **Inter Tight** for headlines — condensed impact
5. **Near-black background** (`#0A0A0A`)
6. **Uppercase labels** with `tracking-wider`, monospace
7. **Monospace for stats/technical** data
8. **1.5% opacity fractal noise** texture overlay
9. **Fast decisive motion** — 150-500ms only
10. **No shadows anywhere** — completely flat

## Anti-Patterns

- No rounded corners
- No traditional shadows
- No multiple accent colors
- No decorative illustrations
- No small/timid headlines (go big or go home)
- No slow animations
- No soft/subtle aesthetic
