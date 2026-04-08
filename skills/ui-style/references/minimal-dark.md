# Minimal Dark

> "Atmospheric depth through carefully orchestrated layers of darkness." Premium developer tools aesthetic (Linear, Raycast, Arc).

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#0A0A0F` | Deep slate base |
| Background Alt | `#12121A` | Elevated surfaces |
| Foreground | `#FAFAFA` | Near-white text |
| Muted BG | `#1A1A24` | Card backgrounds |
| Muted FG | `#71717A` | Secondary text |
| Accent | `#F59E0B` | Warm amber (sole chromatic focus) |
| Accent Muted | `rgba(245,158,11,0.15)` | Amber glow backgrounds |
| Border | `rgba(255,255,255,0.08)` | 8% opacity |
| Border Hover | `rgba(255,255,255,0.15)` | 15% opacity |
| Card | `rgba(26,26,36,0.6)` | Semi-transparent 60% |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Display | **Space Grotesk** | 500-700 | Geometric, technical |
| Body | **Inter** | 400-500 | Clean readability |
| Code | **JetBrains Mono** | 400 | Monospace |

- Scale: 12px to 96px (0.75rem to 6rem)
- Hero: `text-4xl` to `text-6xl`

## Border Radius

| Size | Value |
|------|-------|
| sm | 6px |
| md | 8px (default) |
| lg | 12px |
| xl | 16px |
| 2xl | 24px |
| full | 9999px (pills) |

## Shadows

```css
/* Standard elevation */
box-shadow: 0 4px 16px rgba(0, 0, 0, 0.3);

/* Amber glow (small) */
box-shadow: 0 0 20px rgba(245, 158, 11, 0.15);

/* Amber glow (medium) */
box-shadow: 0 0 40px rgba(245, 158, 11, 0.2);

/* Amber glow (large) */
box-shadow: 0 0 60px rgba(245, 158, 11, 0.25);
```

## Glass Cards

```css
.glass-card {
  background: rgba(26, 26, 36, 0.6);
  backdrop-filter: blur(8px);
  border: 1px solid rgba(255, 255, 255, 0.08);
}
```

## Spacing

- Section padding: `py-24` minimum
- Card padding: `p-6` to `p-8`
- Container: `max-w-6xl`
- Generous section gaps

## Component Patterns

### Buttons
- Primary: amber bg, dark text
- Ghost: transparent, border at 8% opacity
- Hover: amber glow + brightness increase
- Active: `scale-98`
- `px-5 py-2.5`, `font-medium`

### Cards
- Glass effect: semi-transparent bg + backdrop-blur
- Subtle border at 8% opacity
- Hover: `scale-[1.02]` + border brightens to 15%
- Amber glow on featured cards

### Inputs
- Dark bg, subtle border
- Focus: amber border + amber glow
- Placeholder in muted color

### Badges
- Amber-tinted background (`rgba(245,158,11,0.15)`)
- Pulsing dot indicator
- Amber text

## Animation

- Buttons: 200ms `ease-out`
- Cards: 300ms hover scale
- Hover scale: `1.02` on cards
- Active scale: `0.98` on buttons
- Pulsing dot: 2s cycle on badges

## Background Atmosphere

Fixed ambient orbs positioned absolutely:
- Large blur shapes (`blur-3xl`)
- Amber tinted at 5-10% opacity
- Positioned at corners/edges
- Static or very slow drift

## Signature Elements

1. **Minimum 3 dark tones** — `#0A0A0F`, `#12121A`, `#1A1A24`
2. **Warm amber accent** (`#F59E0B`) exclusively
3. **Ambient glow effects** on hover/focus (20-60px radius)
4. **Glass-effect cards** with `backdrop-blur`
5. **Subtle borders** at 8-15% opacity
6. **Fixed ambient orbs** as background atmosphere
7. **Noise texture** at 1.5% opacity
8. **Space Grotesk + Inter + JetBrains Mono** trio

## Anti-Patterns

- No bright/saturated backgrounds
- No more than one accent color (amber only)
- No missing glow effects on interactive elements
- No hard/sharp shadows
- No pure black or pure white
- No missing atmospheric depth (orbs, gradients)
