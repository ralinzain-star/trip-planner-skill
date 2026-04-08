# Enterprise

> Modern enterprise SaaS combining professional credibility with vibrant visual energy. Trustworthiness, dimensional depth, refined elegance.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | Slate 50 (`#F8FAFC`) | Primary canvas |
| Surface | White (`#FFFFFF`) | Card backgrounds |
| Primary | Indigo 600 (`#4F46E5`) | CTAs, focus |
| Secondary | Violet 600 (`#7C3AED`) | Gradients, accents |
| Foreground | Slate 900 (`#0F172A`) | Primary text |
| Muted | Slate 500 (`#64748B`) | Secondary text |
| Border | Slate 200 (`#E2E8F0`) | Borders |

Indigo-to-violet gradient for primary elements.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| All text | **Plus Jakarta Sans** | 400-800 | Modern geometric |

- Scale: Major Third ratio
- Display: ExtraBold (800)
- Body: Regular (400), `leading-[1.6]` to `leading-[1.7]`
- Hero: `text-4xl` to `text-6xl`

## Border Radius

- Cards: `rounded-xl` (12px)
- Buttons: `rounded-full` (pill)
- Inputs: `rounded-lg`

## Shadows (Colored Tints)

```css
/* Card (indigo-tinted) */
box-shadow: 0 4px 20px -2px rgba(79, 70, 229, 0.1);

/* Card hover */
box-shadow: 0 8px 30px -4px rgba(79, 70, 229, 0.15);

/* Violet variant */
box-shadow: 0 4px 20px -2px rgba(124, 58, 237, 0.1);
```

Never use neutral gray shadows — always tinted with the palette.

## Spacing

- Container: `max-w-7xl`
- Section padding: `py-20` to `py-32`
- Card padding: `p-6` to `p-8`
- Responsive padding: `px-4 sm:px-6`

## Component Patterns

### Buttons
- Primary: indigo-to-violet gradient bg, white text, `rounded-full`
- Hover: shadow enhancement + slight brightness
- `px-6 py-3`, `font-semibold`

### Cards
- White bg, subtle indigo-tinted shadow
- `rounded-xl`, `p-6` to `p-8`
- Hover: `-translate-y-1` lift + shadow deepens
- Optional gradient border accent

### Inputs
- White bg, slate border
- Focus: indigo border + indigo ring
- `rounded-lg`, `h-12`

## Distinctive Features

1. **Isometric 3D transforms** — perspective-based rotation on hero elements
2. **Colored shadow system** — indigo/violet tinted, never neutral
3. **Atmospheric blur orbs** — positioned absolutely, layered depth, low opacity
4. **Gradient text** — `bg-clip-text text-transparent bg-gradient-to-r from-indigo-600 to-violet-600`
5. **Elevated card interactions** — `-translate-y-1` + shadow enhancement

## Animation

- Duration: 200-300ms
- Easing: `ease-out`
- Cards: `-translate-y-1` on hover
- Buttons: subtle shadow intensification
- Entrance: staggered fade-in from below
- 3D hero: subtle rotation on scroll/mouse

## Layout

- Mobile-first responsive
- `max-w-7xl` container
- Progressive typography scaling
- Generous section spacing

## Accessibility

- WCAG AA compliance
- `focus-visible` rings on all interactive elements
- Semantic HTML
- `prefers-reduced-motion` support
- High contrast text (Slate 900 on Slate 50)

## Anti-Patterns

- No flat/neutral shadows (always colored)
- No small/tight typography
- No missing background orbs/atmosphere
- No sharp corners on buttons (always pill)
- No single-tone palette (needs the gradient range)
