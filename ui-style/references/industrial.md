# Industrial (Skeuomorphism)

> Celebrates "tactile precision, mechanical reliability, and the soul of physical objects." Interfaces feel like precision instruments from a spacecraft or 1980s synthesizer.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Chassis | `#e0e5ec` | Matte industrial grey background |
| Panel | `#f0f2f5` | Raised panel surfaces |
| Recessed | `#d1d9e6` | Sunken areas, inputs |
| Text Primary | `#2d3436` | Dark charcoal |
| Text Muted | `#4a5568` | Secondary labels |
| Accent | `#ff4757` | Safety Orange/Red — interactive, LEDs, alerts |
| Shadow Dark | `#babecc` | Neumorphic shadow |
| Shadow Light | `#ffffff` | Neumorphic highlight |

**Dark Panels:** `#2d3436` bg, white primary text, `#a8b2d1` secondary text.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Primary | **Inter** | 400-800 | UI text |
| Monospace | **JetBrains Mono** | 400-500 | Numeric displays, data |

- Hero: `text-5xl` to `text-7xl`, weight 800, `tracking-[-0.03em]`
- Labels: `text-xs` to `text-sm`, weight 700, `tracking-[0.05em]` to `tracking-[0.08em]`, UPPERCASE
- Text emboss: `drop-shadow-[0_1px_0_#ffffff]` on light backgrounds

## Border Radius

| Size | Value |
|------|-------|
| sm | 4px |
| md | 8px |
| lg | 16px |
| xl | 24px |
| 2xl | 30px+ |
| full | 9999px |

Soft injection-molded aesthetic — generous rounding.

## Shadows (Neumorphic Dual-Shadow — 45° Top-Left Lighting)

```css
/* Card (raised panel) */
box-shadow: 8px 8px 16px #babecc, -8px -8px 16px #ffffff;

/* Floating (elevated) */
box-shadow: 12px 12px 24px #babecc, -12px -12px 24px #ffffff,
            inset 1px 1px 0 rgba(255,255,255,0.5);

/* Pressed (input/active) */
box-shadow: inset 6px 6px 12px #babecc, inset -6px -6px 12px #ffffff;

/* Recessed (inset area) */
box-shadow: inset 4px 4px 8px #babecc, inset -4px -4px 8px #ffffff;

/* LED Glow */
box-shadow: 0 0 10px 2px rgba(255, 71, 87, 0.6);
```

## Component Patterns

### Buttons ("Physical Keys")
- Primary: `#ff4757` bg, uppercase, wide tracking
- Rim: `rgba(255,255,255,0.2)` border highlight
- Active: `translate-y-[2px]` + shadow inverts to pressed, 150ms
- Min height: 48px

### Cards ("Bolted Modules")
- `#e0e5ec` bg, 16px radius, neumorphic card shadow
- **Corner screws**: radial gradient circles at 12px from each corner
- **Vent slots**: 3 vertical pills (1x24px) with inset shadow
- Hover: `-translate-y-1`, 300ms

### Inputs ("Data Slots")
- Recessed shadow (deeply inset), no border
- Monospace font
- 56px min height, 24px horizontal padding
- Focus: recessed shadow + `0 0 0 2px var(--accent)` LED ring

### LED Indicators
- 8-12px diameter circles
- `animate-pulse` 2s cycle
- Glow shadow in green/red/yellow
- Monospace labels

## Textures

```css
/* CRT Scanlines */
background: repeating-linear-gradient(
  0deg, rgba(18,16,16,0) 50%, rgba(0,0,0,0.25) 50%
);
background-size: 100% 4px;

/* Carbon Fiber */
/* Use transparenttextures.com pattern, 10-20% opacity, mix-blend-mode: overlay */

/* Noise */
/* SVG fractal noise, 20-30% opacity, mix-blend-mode: overlay */
```

## Animation

- Primary easing: `cubic-bezier(0.175, 0.885, 0.32, 1.275)` — mechanical spring
- Button press: 150ms
- Card hover: 300ms
- Image hover: 500ms grayscale → color
- LED pulse: 2s cycle
- Loading: `animate-spin` 1s

## Signature Elements

1. **Corner screw heads** — radial gradient circles at card corners
2. **Vent slots** — vertical pill shapes with inset shadows
3. **CRT scanlines** overlay
4. **Carbon fiber texture** overlay
5. **LED indicators** — pulsing colored dots
6. **Hero device visualization** — CSS-built 3D mockup with bezel
7. **Masking tape/stickers** — `skew-x-12` decorative labels
8. **Push pins** on testimonial cards
9. **Grayscale → color** image treatment on hover
10. **Pipe connectors** for step flows

## Anti-Patterns

- No flat/minimal styling
- No thin/subtle elements
- No missing physical details (screws, vents, LEDs)
- No standard card/button patterns (must feel industrial)
