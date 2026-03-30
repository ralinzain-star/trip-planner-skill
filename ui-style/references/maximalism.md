# Maximalism / Dopamine

> "MORE IS MORE." Rejects minimalist restraint for sensory overload, visual abundance, and unapologetic excess. "Like eating Skittles while watching fireworks."

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#0D0D1A` | Deep cosmic purple-black |
| Foreground | `#FFFFFF` | Pure white |
| Muted | `#2D1B4E` | Dark purple containers |
| Accent 1 | `#FF3AF2` | Electric magenta |
| Accent 2 | `#00F5D4` | Digital cyan |
| Accent 3 | `#FFE600` | Attention yellow |
| Accent 4 | `#FF6B35` | Warm orange |
| Accent 5 | `#7B2FFF` | Mystical purple |

Sections rotate through 5 accents using modulo arithmetic. Borders CLASH with backgrounds intentionally.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Outfit** or **Unbounded** | 700-900 | Impact |
| Body | **DM Sans** | 400-700 | Readable |
| Display (rare) | **Bangers** or **Bungee** | 400 | Maximum impact |

- Hero: 72-128px
- Body: 18-20px
- 20-30% of headlines: animated gradient text

## Text Shadows (Critical)

```css
/* Triple stack */
text-shadow: 2px 2px 0px #7B2FFF,
             4px 4px 0px #FF3AF2,
             6px 6px 0px #00F5D4;
```

## Border Radius

- Buttons: `rounded-full` (9999px)
- Cards: `rounded-3xl` (24px)
- Containers: `rounded-2xl` (16px)

## Borders

- 4px standard, 8px heavy
- Mix solid (70%), dashed (30%), dotted, double within sections
- Border colors CLASH with backgrounds (magenta bg → yellow border)

## Shadows (Dual System)

```css
/* Glow (soft colored) */
box-shadow: 0 0 20px rgba(255, 58, 242, 0.5);

/* Hard stacked offsets */
box-shadow: 8px 8px 0 #FFE600, 16px 16px 0 #FF3AF2;
```

Both glow AND hard offset used simultaneously on key elements.

## Animation (Constant Motion)

- **Float**: 6s ease-in-out infinite
- **Pulse-glow**: 2s ease-in-out infinite
- **Gradient-shift**: 4s linear infinite
- **Spin-slow**: 20s linear infinite
- **Wiggle**: 1s ease-in-out infinite
- **Bounce-subtle**: 2s ease-in-out infinite
- Easing: `cubic-bezier(0.68, -0.55, 0.265, 1.55)` — bouncy

## Signature Elements (Non-Negotiable)

1. **5-10 floating shapes per section** — animated SVG circles, stars, emoji
2. **Oversized background typography** — 12-20rem, opacity-20
3. **Minimum 2 overlapping patterns per section**
4. **Color rotation per section** — modulo 5 through accent palette
5. **Clashing borders** — magenta bg = yellow border
6. **Multi-layer shadows** — minimum 2-3 per element
7. **Asymmetric positioning** — translate-y offsets, rotations
8. **Mixed border styles** (solid + dashed) within sections
9. **Animated emoji decoration** — `text-6xl` to `text-7xl`, floating
10. **Animated gradient text** on 20-30% of headlines

## Anti-Patterns

- **NO minimalism** — if it looks clean, add more
- No restrained palettes — use all 5 accents
- No consistent border styles (variation IS the style)
- No empty space — fill it with floating shapes
- No subtle anything
- No static elements — something must always be moving
