# Flat Design

> "The Z-axis does not exist. Everything is on the same plane." Hierarchy through size, color, and typography only.

## Color Palette (Light Mode)

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FFFFFF` | Primary canvas |
| Foreground | `#111827` | Primary text |
| Primary | `#3B82F6` | Blue — CTAs and links |
| Secondary | `#10B981` | Emerald — success/positive |
| Accent | `#F59E0B` | Amber — highlights |
| Muted BG | `#F3F4F6` | Gray 100 — secondary surfaces |
| Muted FG | `#6B7280` | Gray 500 — secondary text |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| All text | **Outfit** | 400-800 | Sans-serif |

- Headings: 700-800 weight, tight spacing (`-0.02em`)
- Body: 400 weight, relaxed leading
- Hero: `text-4xl` to `text-6xl`

## Border Radius

- Buttons: `rounded-md`
- Cards: `rounded-md` to `rounded-lg`
- Inputs: `rounded-md`
- Moderate rounding — not too sharp, not too round

## Shadows

**ABSOLUTELY NO BOX SHADOWS ON ELEMENTS.** This is the defining rule of flat design.

Gradients restricted to subtle background decoration only — never on components.

## Borders

- Subtle: `border border-gray-200`
- Color accents: `border-2 border-primary` on focus/active
- Section dividers: `border-t border-gray-200`

## Spacing

- Section padding: `py-16` to `py-24`
- Card padding: `p-6` to `p-8`
- Container: `max-w-6xl`
- Alternate section backgrounds: white → gray → bold color

## Component Patterns

### Buttons
- Solid color background, no shadow
- `rounded-md`, `px-6 py-3`
- Hover: `hover:scale-105` + color brightness change
- Immediate color fills, no fades
- Secondary: transparent with `border-2`

### Cards (Color Block Style)
- Solid background color (white or muted)
- NO shadows
- Generous padding
- Hover: `scale(1.02)` + background color shift
- Section-based color blocking

### Inputs
- `bg-gray-100` background
- `border-2 border-transparent`
- Focus: `border-2 border-primary` (solid primary color)
- No shadow, no glow

### Sections
- Alternate backgrounds: white / gray / bold accent color
- Sharp transitions between sections (no gradients)
- Full-width color blocks

## Animation

- `transition-all duration-200`
- Hover: color shifts, `scale-105`, immediate color fills
- No fade transitions — instant switches
- No parallax, no float, no depth effects

## Signature Elements

1. **Zero shadows** — hierarchy through color and size only
2. **Bold color blocks** — sections with full-width solid backgrounds
3. **Geometric shapes only** — rectangles, circles, squares (no organic)
4. **Strong color contrast** — bright primaries on white
5. **Scale interaction** — `scale-105` hover, `scale-95` active
6. **Alternating section backgrounds** — visual rhythm through color

## Anti-Patterns

- **NO box shadows** on any element — this is the most critical rule
- No gradients on components (background only, subtle)
- No organic shapes — strictly geometric
- No depth or layering effects
- No transparency/opacity effects on surfaces
- No blur effects
- No 3D transforms
