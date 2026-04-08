# Web3 / Bitcoin DeFi

> "Sophisticated fusion of precision engineering, cryptographic trust, and digital gold." Secure, Technical, Valuable.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| True Void | `#030304` | Primary background |
| Dark Matter | `#0F1115` | Cards, panels |
| Pure Light | `#FFFFFF` | Primary text |
| Stardust | `#94A3B8` | Secondary text |
| Dim Boundary | `#1E293B` | Subtle borders |
| Bitcoin Orange | `#F7931A` | Primary CTAs, trust |
| Burnt Orange | `#EA580C` | Gradients, secondary |
| Digital Gold | `#FFD600` | Value indicators, success |

Signature gradients:
- `linear-gradient(to right, #EA580C, #F7931A)`
- `linear-gradient(to right, #F7931A, #FFD600)`

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Space Grotesk** | 400-700 | Technical precision |
| Body | **Inter** | 400-600 | Clean readability |
| Stats/Code | **JetBrains Mono** | 400-500 | Data display |

- Hero: `text-4xl` mobile to `text-7xl` desktop
- Body: `text-base` to `text-lg`

## Border Radius

- Cards: `rounded-2xl` (16px)
- Buttons: `rounded-full` (pill)
- Inputs: `rounded-lg` (8px)

## Shadows (Orange/Gold Tinted — Never Pure Black)

```css
/* Primary glow */
box-shadow: 0 0 20px -5px rgba(234, 88, 12, 0.5);

/* Hover intensified */
box-shadow: 0 0 30px -5px rgba(247, 147, 26, 0.6);

/* Gold accent */
box-shadow: 0 0 20px -5px rgba(255, 214, 0, 0.3);
```

## Glass Morphism

```css
.web3-glass {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.08);
}
```

## Component Patterns

### Buttons
- Orange gradient bg, white text, pill shape
- Hover: glow intensifies + slight lift
- `px-6 py-3`, `font-semibold`

### Cards
- Dark matter bg, subtle border
- Corner border accents: `border-t border-l` in Bitcoin orange
- Hover: orange glow + `-translate-y-1`
- Glass morphism variants

### Badges
- Animated `ping` effect (pulsing ring)
- Orange/gold gradient backgrounds
- Small, eye-catching

## Animation

- Float: 8s ease-in-out (background elements)
- Orbital spin: 10s (outer ring), 15s reverse (inner ring)
- Bounce cards: 3-4s staggered
- Card lift: `-translate-y-1`, 300ms
- Ping badges: continuous pulsing

## Signature Elements

1. **Gradient text on headlines** — orange-to-gold on final 1-2 words
2. **Spinning orbital rings** in hero — 10s/15s reverse rotation
3. **Corner border accents** — partial borders in Bitcoin orange
4. **Glowing animated badges** with `animate-ping`
5. **Background icon watermarks** — opacity shift on hover
6. **Blockchain timeline** — vertical gradient line with numbered nodes
7. **Asymmetric pricing** — popular tier at `scale-105`
8. **Glass morphism** + visible grid backgrounds
9. **Colored shadows only** — orange/gold tints
10. **Grid pattern backgrounds** at low opacity

## Anti-Patterns

- No cool-toned accents (orange/gold family only)
- No pure black shadows (always tinted)
- No generic flat design (must feel Web3-native)
- No rounded-lg on buttons (always pill)
- No missing orbital/particle animations in hero
