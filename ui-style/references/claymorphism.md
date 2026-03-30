# Claymorphism

> "Digital clay" — premium, tactile, playful interface with high-fidelity depth simulation.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Canvas | `#F4F1FA` | Pale lavender-white background |
| Text Primary | `#332F3A` | Soft charcoal |
| Text Secondary | `#635F69` | Muted charcoal |
| Violet | `#7C3AED` | Primary accent |
| Hot Pink | `#EC4899` | Secondary accent |
| Sky Blue | `#38BDF8` | Tertiary accent |
| Emerald | `#10B981` | Success/positive |
| Amber | `#F59E0B` | Warning/highlight |

- All accent colors are vivid and saturated
- Canvas is never pure white — always has a tint

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Nunito** | 700-900 | Rounded terminals enhance softness |
| Body | **DM Sans** | 400-700 | Geometric clarity |

- Hero scale: `text-5xl` to `text-8xl`, tight leading (`leading-[1.1]`)
- Body: `text-base` to `text-lg`, relaxed leading

## Border Radius

- **Minimum `rounded-[20px]`** — nothing less
- Cards: `rounded-[32px]` typical
- Buttons: `rounded-[16px]` to `rounded-full`
- Inputs: `rounded-[16px]`
- Never use small radii (`rounded-sm`, `rounded-md`) — they break the clay feel

## Shadows (Critical — 4-Layer System)

The clay effect comes from multi-layered shadow stacks simulating matte-finish materials with top-left diffused lighting:

```css
/* Clay Card */
.clay-card {
  box-shadow:
    8px 8px 16px rgba(0, 0, 0, 0.08),
    -4px -4px 12px rgba(255, 255, 255, 0.6),
    inset 1px 1px 2px rgba(255, 255, 255, 0.4),
    inset -1px -1px 2px rgba(0, 0, 0, 0.04);
}

/* Clay Card Hover (more pronounced) */
.clay-card:hover {
  box-shadow:
    12px 12px 24px rgba(0, 0, 0, 0.1),
    -6px -6px 16px rgba(255, 255, 255, 0.7),
    inset 1px 1px 2px rgba(255, 255, 255, 0.5),
    inset -1px -1px 2px rgba(0, 0, 0, 0.05);
}

/* Pressed/Active */
.clay-pressed {
  box-shadow:
    inset 4px 4px 8px rgba(0, 0, 0, 0.08),
    inset -2px -2px 6px rgba(255, 255, 255, 0.4),
    2px 2px 4px rgba(0, 0, 0, 0.04),
    -1px -1px 3px rgba(255, 255, 255, 0.3);
}
```

## Spacing

- Section padding: `py-20` to `py-32`
- Card padding: `p-8` to `p-10`
- Component gaps: `gap-6` to `gap-8`
- Container: `max-w-6xl`

## Component Patterns

### Buttons
- Accent background with clay shadow
- Hover: lift `-translate-y-1` to `-translate-y-3` + enhanced shadow
- Active: `scale-[0.92]` + pressed shadow (200ms squish)
- `px-6 py-3`, `font-bold`, rounded-full or rounded-[16px]

### Cards
- Canvas-colored background with full clay shadow stack
- Rounded-[32px], generous padding
- Hover: gentle lift + shadow enhancement
- Optional: colored accent border or gradient top

### Inputs
- Inset clay shadow (pressed into surface)
- `rounded-[16px]`, generous padding
- Focus: subtle glow in accent color

## Animation

- Hover lift: `-translate-y-1` to `-translate-y-3` + shadow enhancement
- Active press: `scale-[0.92]` + pressed shadow, 200ms
- Background drift: 8-12s float cycles with subtle rotation
- Breathing stat orbs: 6s scale oscillation
- Easing: `cubic-bezier(0.4, 0, 0.2, 1)` for smooth organic feel
- Duration: 200-300ms for interactions, 6-12s for ambient

## Signature Elements

1. Multi-layered shadow stacks (4 layers minimum)
2. Top-left diffused lighting model
3. Large border radius everywhere (minimum 20px)
4. Vivid saturated accent colors on soft canvas
5. Tactile press/squish feedback on buttons
6. Floating background shapes with drift animation
7. Breathing/pulsing accent orbs

## Anti-Patterns

- No flat shadows (single layer)
- No sharp corners anywhere
- No thin borders as primary definition
- No dark mode (claymorphism works best on light surfaces)
- No pure white canvas — always tinted
- Don't reduce radii on mobile

## Responsive Notes

Mobile-first design. Never flatten depth or reduce radii aggressively on smaller screens — the clay feel must persist.
