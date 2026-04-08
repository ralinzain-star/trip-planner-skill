# Newsprint

> "Absolute clarity, hierarchy, and structure" through high-contrast typography, grid-based layouts, and sharp geometric precision.

## Color Palette (Light Mode Only)

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#F9F9F7` | Warm off-white paper |
| Foreground | `#111111` | Ink black |
| Accent | `#CC0000` | Editorial red (sparingly) |
| Divider | `#E5E5E0` | Light grey |

Strictly limited — paper, ink, and one spot color.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headlines | **Playfair Display** | 400-900 | High-contrast serif |
| Body | **Lora** | 400-700 | Readable serif |
| UI/Labels | **Inter** | 400-600 | Clean sans-serif |
| Data | **JetBrains Mono** | 400-500 | Monospace |

- Hero H1: `text-9xl` on desktop, `leading-[0.9]` tight
- Body: `text-lg`, `leading-relaxed`, `text-justify` in columns
- Labels: `uppercase tracking-widest text-xs font-mono`

## Border Radius

**Zero everywhere.** Sharp 90-degree corners.

## Shadows

Hard offset only on hover:

```css
/* Hover shadow */
box-shadow: 4px 4px 0px #111111;
/* With translate to maintain position */
transform: translate(-2px, -2px);
```

No shadows at rest.

## Borders

- Section dividers: `border-b` or `border-r`
- Collapsed borders on grids (shared lines)
- Thick dividers: `border-b-2` between major sections

## Spacing

- Container: `max-w-screen-xl` (1280px)
- Card padding: `p-6` to `p-8`
- Grid gaps: `gap-6` to `gap-8`
- Tight, efficient use of space (newspaper density)

## Component Patterns

### Buttons
- Black bg, white text, sharp corners
- Hover: full inversion
- UPPERCASE, tracked, sans-serif
- Red accent variant for CTAs

### Cards
- 12-column grid with collapsed borders (shared border lines)
- No individual card borders — grid borders define cells
- Vertical dividers (`border-r`) between columns

### Inputs
- Bottom border only (`border-b-2`)
- Focus: border darkens/thickens
- Clean, minimal styling

### Images
- Default: `grayscale`
- Hover: `sepia` with transition
- Captions in italic serif below

## Layout

- **Multi-column body text**: `columns-2` or `columns-3` with `text-justify`
- Newspaper grid: 12-column with shared border lines
- Vertical grid dividers between columns
- Dense packing — minimize whitespace

## Signature Elements

1. **Justified multi-column text** — newspaper layout
2. **Drop caps** — massive first letter of articles
3. **Dot grid background**: `radial-gradient(#ddd 1px, transparent 1px); background-size: 4px 4px`
4. **Grayscale images** — sepia on hover
5. **Vertical column dividers** — `border-r`
6. **Edition metadata** — publication date, volume, issue number
7. **At least one inverted section** — black bg, white text
8. **Uppercase mono labels** — `tracking-widest text-xs`
9. **Hard offset shadow on hover** — with translate
10. **Editorial red** — used sparingly for emphasis

## Animation

- Fast, snappy, mechanical
- `duration-200 ease-out`
- Buttons: color inversion
- Cards: hard shadow appears
- Links: red underline appears
- No bouncy easing

## Accessibility

- Black on off-white = AAA contrast (>17:1)
- Focus: thick black ring, 2px offset
- Touch targets: 44x44px minimum
