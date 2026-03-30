# Monochrome

> "Reduction to Essence." Strips design to its most fundamental elements: black, white, and typography.

## Color Palette (Absolute — No Other Colors Permitted)

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FFFFFF` | Primary page bg |
| Foreground | `#000000` | Primary text & elements |
| Muted BG | `#F5F5F5` | Secondary backgrounds |
| Muted FG | `#525252` | Secondary text |
| Accent | `#000000` | Black IS the accent |
| Accent FG | `#FFFFFF` | Text on black |
| Border | `#000000` | Standard borders |
| Border Light | `#E5E5E5` | Subtle dividers |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Display/Headlines | **Playfair Display** | 400-900 | High-contrast serif |
| Body | **Source Serif 4** | 400-600 | Readable serif |
| Labels/Mono | **JetBrains Mono** | 400-500 | Technical elements |

- Headlines: `tracking-tight` to `tracking-tighter`
- Body: `leading-relaxed` (1.625)
- Labels: `tracking-widest` (0.1em), uppercase
- Hero: `text-8xl` to `text-9xl` (128-160px)

## Border Radius

**`0px` globally.** No rounding anywhere.

## Shadows

**None whatsoever.** Depth via color inversion, border weight, scale contrast, negative space.

## Borders

| Weight | Usage |
|--------|-------|
| Hairline: 1px `#E5E5E5` | Subtle dividers |
| Thin: 1px `#000` | Standard borders |
| Medium: 2px | Emphasis borders |
| Thick: 4px | Section dividers |
| Ultra: 8px | Major divisions |

## Textures (6 Patterns)

```css
/* 1. Horizontal lines */
background: repeating-linear-gradient(0deg, rgba(0,0,0,0.015) 0 1px, transparent 1px 4px);

/* 2. Grid */
background-image: repeating-linear-gradient(0deg, rgba(0,0,0,0.015) 0 1px, transparent 1px 40px),
                  repeating-linear-gradient(90deg, rgba(0,0,0,0.015) 0 1px, transparent 1px 40px);

/* 3. Diagonal lines */
background: repeating-linear-gradient(45deg, rgba(0,0,0,0.01) 0 1px, transparent 1px 40px);

/* 4. Noise */
/* SVG fractal noise, 2% opacity */

/* 5. Vertical lines (for inverted sections) */
background: repeating-linear-gradient(90deg, rgba(255,255,255,0.03) 0 1px, transparent 1px 4px);

/* 6. Radial gradient (dark CTA sections) */
background: radial-gradient(circle at top center, rgba(255,255,255,0.05), transparent 60%);
```

## Spacing

- Container: `max-w-6xl` (72rem / 1152px)
- Horizontal: `px-6` to `px-12`
- Section: `py-24` to `py-40`
- Section dividers: 4px or 8px solid black

## Component Patterns

### Buttons
- `#000` bg, `#FFF` text, uppercase, `tracking-widest`
- `px-8 py-4`, `rounded-none`
- Hover: full inversion (white bg, black text), 100ms
- Focus: 3px solid outline, 3px offset

### Cards
- 1px solid `#000` border, no shadow
- Hover: full color inversion (100ms instant)
- Inverted variant: `#000` bg, `#FFF` text

### Inputs
- 2px solid `#000` (bottom or full border)
- Placeholder: `#525252`, italic
- Focus: border thickens to 3-4px

### Icons
- Outlined style, strokeWidth 1-1.5
- Always `#000000`, 20-24px

## Animation

- **Minimal and Instant.** 0-100ms maximum.
- Cards: 100ms color inversion
- Blog images: 300ms border 2px → 4px + scale 105%
- No bouncy, no parallax, no slow easing
- Binary transitions — on/off, not gradual

## Signature Elements

1. **Oversized hero typography** (8xl-9xl)
2. **Color inversion on hover** — instant black↔white swap
3. **Inverted stats section** — black bg, white text, vertical line texture
4. **Heavy 4px horizontal dividers** between sections
5. **Editorial pull quotes** — large italic serif + oversized quotation marks
6. **Drop caps** — boxed, first letter of content sections
7. **Zero accent colors** — black is the only accent
8. **Typography as graphics** — type IS the visual
9. **Layered textures** (subtle, low opacity)
10. **Thickening image borders** on hover (2px → 4px)

## Anti-Patterns

- **NO colors** of any kind — only black, white, gray
- No shadows
- No rounded corners
- No gradients
- No illustrations or decorative graphics
- No slow animations
