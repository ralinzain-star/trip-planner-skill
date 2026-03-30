# Luxury Editorial

> "Elegance through restraint, precision, and depth." Luxury isn't about adding decoration — it's about removing everything unnecessary and perfecting what remains.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#F9F8F6` | Warm Alabaster |
| Foreground | `#1A1A1A` | Rich Charcoal (not pure black) |
| Muted BG | `#EBE5DE` | Pale Taupe |
| Muted FG | `#6C6863` | Warm Grey |
| Accent | `#D4AF37` | Metallic Gold |
| Accent FG | `#FFFFFF` | Text on gold |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Playfair Display** | 400-700 | Transitional serif |
| Body | **Inter** | 400-500 | Humanist sans-serif |

- Hero: `text-6xl` to `text-9xl`
- Body: `text-base` to `text-lg`, `leading-relaxed`
- Labels: `tracking-[0.25em]` to `tracking-[0.3em]`, uppercase, `text-xs`

## Border Radius

**`0px` EVERYWHERE.** Strict rectangularity. No rounded corners at all.

## Borders

- Width: always `1px`
- Single borders (top or bottom) preferred over full boxes
- Color: warm border or gold accent

## Shadows

```css
/* Hero images */
box-shadow: 0 8px 32px rgba(0, 0, 0, 0.12);

/* Feature images */
box-shadow: 0 4px 24px rgba(0, 0, 0, 0.08);

/* Cards (default) */
box-shadow: 0 2px 8px rgba(0, 0, 0, 0.02);

/* Cards (hover) */
box-shadow: 0 8px 24px rgba(0, 0, 0, 0.06);
```

Paper texture: subtle SVG noise at 2% opacity overlay.

## Spacing

- Section padding: `py-24` to `py-40`
- Card padding: `p-8` to `p-12`
- Container: `max-w-6xl`
- Extreme whitespace — luxury breathes

## Component Patterns

### Buttons
- Rectangular `rounded-none`, `h-12` (48px)
- Uppercase `text-xs`, `tracking-[0.2em]`
- Primary: gold background, white text
- Hover: gold overlay slides from left (`duration-500`)
- Secondary: transparent with 1px border

### Cards
- White background, `border-t` or `border-b` only
- Subtle shadow, deepens on hover
- No full border boxes — partial borders only

### Images
- Default grayscale: `grayscale`
- Hover: `grayscale-0` full color + `scale-105`
- Transition: `duration-[1500ms]` to `duration-[2000ms]` (ultra-slow, cinematic)

## Animation

- Buttons: `duration-500`
- Color transitions: `duration-700`
- Image transitions: `duration-[1500ms]` to `duration-[2000ms]`
- Easing: `ease-out` or `cubic-bezier(0.25, 0.46, 0.45, 0.94)`
- **Never** `ease-in-out`

## Signature "Bold Factor" Elements

1. **Vertical text labels** — `writing-mode: vertical-rl` on margins
2. **Drop caps** — Playfair Display, `text-7xl`, `float-left`
3. **Mixed italic headlines** — gold color on italic words
4. **Grayscale-to-color image transitions** with `scale-105`
5. **Visible fixed grid lines** across viewport
6. **Gold sliding animation** on primary buttons
7. **Decorative horizontal lines** — `h-px w-8` to `w-12`
8. **Extreme type scale contrast** — massive headlines + tiny `text-[10px]` labels
9. **Layered shadows** deepening on hover
10. **Testimonial gold border animation** + grayscale avatar reveal

## Anti-Patterns

- **NO rounded corners** — strict rectangularity
- No harsh/heavy shadows
- No pure black or pure white text
- No fast animations (luxury is slow and deliberate)
- No vibrant/saturated colors (only gold accent)
- No centered layouts (asymmetric composition)
- No overcrowded spacing
