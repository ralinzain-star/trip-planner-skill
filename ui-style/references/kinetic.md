# Kinetic Typography

> "Typography as the entire visual structure." Text becomes image, headline becomes hero, motion becomes rhythm.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#09090B` | Rich black |
| Foreground | `#FAFAFA` | Off-white |
| Accent | `#DFE104` | Acid yellow |
| Muted | `#27272A` | Dark zinc |
| Border | `#3F3F46` | Zinc 700 |

Minimal palette — black, white, and one acid accent.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| All text | **Space Grotesk** | 400-700 | Geometric sans |

- ALL display text: UPPERCASE
- Fluid sizing: `clamp(3rem, 12vw, 14rem)` for heroes
- Hero scale: massive — fills the viewport
- Body: `text-base` to `text-lg`

## Border Radius

**`0px` everywhere.** Sharp corners mandatory.

## Borders

- 2px weight standard
- No decorative borders — structural only

## Shadows

**None.** Completely flat — depth through typography scale and motion.

## Spacing

- Base unit: 4px
- Section padding: `py-32` (128px)
- Card padding: `p-8` to `p-12`
- Container: full-width for maximum type impact

## Component Patterns

### Buttons
- Solid background, sharp corners
- Hover: hard color inversion (black ↔ yellow)
- UPPERCASE, bold
- Fast transition: 150ms

### Cards
- Minimal containers — borders only
- Focus on typography within
- Large background numbers (6-12rem) as decoration

### Headlines
- Viewport-spanning type
- `clamp()` for fluid scaling
- Uppercase lockups

## Animation (Core Identity)

1. **Infinite marquees** — `react-fast-marquee`, no gradients, continuous flow
2. **Scroll-triggered transforms** — scale/opacity on scroll entry
3. **Hard color inversions** on hover — black ↔ yellow, instant
4. **Massive background numbers** — 6rem to 12rem, subtle opacity

## Signature Elements

1. **Infinite marquee banners** — text scrolling continuously
2. **Massive type** — headlines fill the screen
3. **Aggressive scale hierarchy** — 8-10x difference between largest and smallest
4. **Uppercase lockups** — all display text capitalized
5. **Constant kinetic energy** — something always moving
6. **Acid yellow accent** — high contrast on black
7. **Background oversized numbers** — decorative, low opacity
8. **Hard hover inversions** — instant color swap

## Anti-Patterns

- No small, timid typography
- No rounded corners
- No shadows or depth effects
- No decorative illustrations (type IS the decoration)
- No slow/subtle animations
- No multiple accent colors
- No standard card-based layouts (typography drives structure)
