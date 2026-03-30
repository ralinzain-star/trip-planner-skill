# Organic / Natural

> Embraces wabi-sabi — acceptance of transience and imperfection. "There are no straight lines in nature." Warmth, softness, natural connection.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FDFCF8` | Off-white rice paper |
| Foreground | `#2C2C24` | Deep loam/charcoal |
| Primary | `#5D7052` | Moss green |
| Primary FG | `#F3F4F1` | Pale mist |
| Secondary | `#C18C5D` | Terracotta/clay |
| Accent BG | `#E6DCCD` | Sand/beige |
| Accent FG | `#4A4A40` | Bark |
| Muted BG | `#F0EBE5` | Stone |
| Muted FG | `#78786C` | Dried grass |
| Border | `#DED8CF` | Raw timber |
| Destructive | `#A85448` | Burnt sienna |

Earth-drawn palette strictly — no deviation.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Fraunces** | 600-800 | Variable serif, old-world warmth |
| Body | **Nunito** or **Quicksand** | 400-500 | Rounded terminals essential |

- Scale: 1.25 modular ratio
- Hero: `text-5xl` to `text-7xl`
- Body: `text-base` to `text-lg`

## Border Radius (Organic Blobs)

- Cards: `rounded-2xl` to `rounded-3xl` (16-24px)
- Buttons/Inputs: `rounded-full` (pill shape)
- **Organic blob shapes** via custom values:

```css
/* Alternating blob patterns for cards */
border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
border-radius: 40% 60% 70% 30% / 30% 70% 40% 60%;
border-radius: 70% 30% 40% 60% / 40% 60% 30% 70%;
/* ... 6 alternating patterns across feature cards */
```

**No 90-degree angles** — all shapes appear eroded/hand-shaped.

## Shadows (Colored — Never Pure Black)

```css
/* Moss-tinted */
box-shadow: 0 4px 20px -2px rgba(93, 112, 82, 0.15);

/* Clay-tinted */
box-shadow: 0 10px 40px -10px rgba(193, 140, 93, 0.2);

/* Moss deep */
box-shadow: 0 20px 50px -15px rgba(93, 112, 82, 0.25);
```

## Global Grain Texture

```css
/* Apply to body — 3-5% opacity, multiply blend */
.grain::before {
  content: '';
  position: fixed;
  inset: 0;
  opacity: 0.04;
  mix-blend-mode: multiply;
  pointer-events: none;
  /* SVG fractal noise or grainy texture */
}
```

## Component Patterns

### Buttons
- Moss green bg, pale text, `rounded-full` (pill)
- Hover: darken + `scale-105` + shadow deepen
- Active: `scale-95` (tactile press)
- `px-6 py-3`, `font-medium`
- Secondary: transparent with moss border

### Cards
- Rice paper or stone bg
- Organic blob border-radius (alternating patterns)
- Colored shadow (moss or clay tinted)
- Hover: `-translate-y-1` or `rotate-1` + shadow deepens

### Inputs
- `rounded-full` (pill shape)
- Moss border on focus
- Soft background

### Images
- Organic blob clip-path or asymmetric border-radius
- Slight rotation offset
- `scale-105` on hover at 700ms

## Animation

- Duration: 300-700ms range
- Hover: `scale-105` + shadow deepen
- Active: `scale-95` (tactile press)
- Card hover: `-translate-y-1` or `rotate-1`
- Image hover: `scale-105` at 700ms
- Gentle, natural motion — nothing harsh

## Spacing

- Container: `max-w-6xl`
- Section: `py-24` to `py-32`
- Gaps: `gap-8`, `gap-12`, `gap-16` — generous
- Content breathes

## Signature Elements

1. **Global grain/noise texture** at 3-5% opacity, multiply blend
2. **Organic blob shapes** — asymmetric border-radius on everything
3. **Colored shadows only** — moss-green or clay-orange tints
4. **Fraunces + Nunito** font pairing
5. **Pill-shaped buttons and inputs** (`rounded-full`)
6. **Soft diffused motion** — minimum 300ms, no harsh snaps
7. **Generous whitespace** — `gap-8` to `gap-16`
8. **No 90-degree angles** — all shapes look naturally eroded
9. **Asymmetry** — rotated images, offset elements, varied card shapes
10. **Earth-drawn palette** strictly

## Anti-Patterns

- No sharp/geometric shapes
- No pure black shadows
- No cold/blue tones
- No fast/snappy animations
- No dense layouts
- No standard rectangular cards
- No system/monospace fonts
