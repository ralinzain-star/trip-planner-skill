# Neumorphism

> "Tactile, calm, modern" — dual opposing shadows creating depth illusion on monochromatic surface.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Base Background | `#E0E5EC` | Primary surface (everything sits on this) |
| Text Primary | `#3D4852` | 7.5:1 contrast ratio |
| Text Secondary | `#6B7B8D` | Muted text |
| Accent | `#6C63FF` | Soft violet — interactive elements |
| Dark Shadow | `rgba(163,177,198,0.6)` | Bottom-right shadow |
| Light Shadow | `rgba(255,255,255,0.5)` | Top-left highlight |

- Everything is monochromatic — the background IS the surface
- Single accent color for interactive elements only

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Display | **Plus Jakarta Sans** | 500-800 | Modern geometric |
| Body | **DM Sans** | 400-700 | Clean readability |

## Border Radius

- Buttons: minimum `rounded-[16px]`
- Cards: minimum `rounded-[32px]`
- Inputs: `rounded-[16px]`
- Everything is rounded — no sharp corners

## Shadows (4-State System — The Core Mechanic)

```css
/* Extruded (raised — default state) */
box-shadow:
  8px 8px 16px rgba(163, 177, 198, 0.6),
  -8px -8px 16px rgba(255, 255, 255, 0.5);

/* Extruded Hover (elevated) */
box-shadow:
  12px 12px 24px rgba(163, 177, 198, 0.6),
  -12px -12px 24px rgba(255, 255, 255, 0.5);

/* Inset (pressed) */
box-shadow:
  inset 6px 6px 12px rgba(163, 177, 198, 0.6),
  inset -6px -6px 12px rgba(255, 255, 255, 0.5);

/* Inset Deep (deeply pressed — active inputs) */
box-shadow:
  inset 8px 8px 16px rgba(163, 177, 198, 0.7),
  inset -8px -8px 16px rgba(255, 255, 255, 0.6);
```

## Borders

**NO borders.** Shadows define ALL edges. This is non-negotiable.

## Spacing

- Section padding: `py-20` to `py-32`
- Card padding: `p-8` to `p-12`
- Container: `max-w-5xl`
- Generous spacing to let shadows breathe

## Component Patterns

### Buttons
- Same background color as surface (`bg-[#E0E5EC]`)
- Extruded shadow (raised appearance)
- Hover: elevated shadow (more pronounced)
- Active: inset shadow (pressed into surface)
- Accent color for text/icon, not background
- `px-8 py-4`, `font-semibold`, `rounded-[16px]`

### Cards
- Same background as page surface
- Extruded shadow creates the "raised" effect
- `rounded-[32px]`, generous padding
- Hover: shadow deepens slightly
- No borders — shadows only

### Inputs
- Inset shadow (pressed into surface)
- Background matches surface
- Focus: accent glow ring + deeper inset
- `rounded-[16px]`, `px-6 py-4`

### Toggles / Switches
- Track: inset shadow (recessed groove)
- Thumb: extruded shadow (raised knob)
- Active: accent-colored thumb

## Animation

- Duration: 200-300ms
- Easing: `ease-out`
- Hover: shadow transition (extruded → elevated)
- Active: shadow transition (extruded → inset), 150ms
- Smooth shadow interpolation is key

## Signature Elements

1. **Dual opposing shadows** — every element has both dark and light shadows
2. **No borders anywhere** — shadows define ALL edges
3. **Monochromatic surface** — elements are the same color as background
4. **Extruded/inset states** — physical metaphor of raising and pressing
5. **Large border radii** — soft, organic shapes
6. **Single accent color** — violet for interactive elements only

## Anti-Patterns

- **NO borders** — shadows define edges, not lines
- No high-contrast background differences between cards and page
- No flat shadows (always dual-direction)
- No sharp corners
- No dark mode (neumorphism requires light surface for shadow visibility)
- No thin or small shadows — they need room to breathe

## Accessibility Notes

- Minimum 44px touch targets for all interactive elements
- Visible focus states with accent color ring
- Text contrast ratio must be 7:1+ despite soft aesthetic
- `prefers-reduced-motion`: reduce shadow transitions
