# Botanical / Organic Serif

> "Digital ode to nature" — soft, sophisticated, deeply intentional. Inspired by botanical gardens, ceramics studios, editorial design. "Whispers rather than shouts."

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#F9F8F4` | Warm alabaster/rice paper |
| Text | `#2D3A31` | Deep forest green |
| Sage | `#8C9A84` | Buttons, highlights, focus |
| Clay | `#DCCFC2` | Card backgrounds |
| Stone | `#E6E2DA` | Subtle borders |
| Terracotta | `#C27B66` | Hover states, CTAs |

All colors drawn from nature — earth, stone, leaf, clay.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Playfair Display** | 600-700 | Transitional serif |
| Body | **Source Sans 3** | 400-500 | Humanist sans |

- Frequent italic emphasis in Playfair headlines
- Hero: `text-4xl` to `text-6xl`
- Body: `text-base` to `text-lg`

## Border Radius

- Cards: `rounded-3xl` (24px)
- Buttons: `rounded-full` (pill)
- Arch imagery: `rounded-t-full` or `rounded-[40px]`

## Shadows

```css
/* Subtle, forest-green tinted */
box-shadow: 0 4px 6px -1px rgba(45, 58, 49, 0.05);

/* Medium */
box-shadow: 0 10px 25px -5px rgba(45, 58, 49, 0.08);

/* Large */
box-shadow: 0 25px 50px -12px rgba(45, 58, 49, 0.15);
```

Always tinted with forest green — never pure black shadows.

## Component Patterns

### Buttons
- Sage bg (`#8C9A84`), white text, pill shape
- Hover: darken to terracotta (`#C27B66`)
- `px-6 py-3`, `font-medium`
- Secondary: transparent with sage border

### Cards
- Clay bg (`#DCCFC2`) or white
- `rounded-3xl`, generous padding
- Stone border (`#E6E2DA`)
- Staggered grid: every 2nd card `translate-y-12` on desktop

### Images
- Arch shape: `clip-path` or `rounded-t-full`
- 200px arch radius via CSS
- Overlapping typography on images

## Paper Grain Texture (CRITICAL)

```css
/* Without this, the design loses its soul */
.paper-grain::before {
  content: '';
  position: fixed;
  inset: 0;
  opacity: 0.015;
  pointer-events: none;
  z-index: 9999;
  /* SVG fractal noise filter */
  background: url("data:image/svg+xml,..."); /* fractal noise SVG */
}
```

## Decorative Elements

```css
/* Fine vine/root lines */
.vine-line {
  height: 1px;
  background: linear-gradient(to right, transparent, #8C9A84, transparent);
}
```

## Animation

- Fast: 300ms
- Standard: 500ms
- Dramatic: 700-1000ms
- Movement feels like "plants swaying in breeze" or "suspended in honey"
- Hover: gentle scale + shadow deepen

## Signature Elements

1. **Paper grain texture** — CRITICAL, fixed full-screen noise at 0.015 opacity
2. **Arch imagery** — CSS clip-path, 200px arch radius
3. **Overlapping typography** — serif headlines layered over images
4. **Decorative fine 1px SVG lines** — mimicking vines/roots
5. **Frequent italic emphasis** in Playfair headlines
6. **Sacred whitespace** — generous `py-32` sections
7. **Staggered grid** — every 2nd card offset vertically (desktop only)
8. **Backdrop-blur** on overlays

## Anti-Patterns

- No vibrant/saturated colors (earth tones only)
- No sharp/geometric shapes
- No cold tones
- No heavy/dark shadows
- No aggressive animations
- No missing paper grain texture
- No dense layouts (breathing room essential)
