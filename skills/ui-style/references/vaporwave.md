# Vaporwave / Outrun

> "Digital Nostalgia meets Neon Future." 1980s retro-futurism, high-contrast maximalism, neon saturation. Simultaneously nostalgic and forward-looking.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#090014` | Near-black with purple tint |
| Foreground | `#E0E0E0` | Silver-gray text |
| Card | `#1a103c` | Deep purple (80% opacity) |
| Hot Magenta | `#FF00FF` | Primary accent |
| Electric Cyan | `#00FFFF` | Links, focus, hover |
| Sunset Orange | `#FF9900` | Special highlights |
| Border | `#2D1B4E` | Muted dark purple |

Signature gradient: `linear-gradient(to right, #FF9900, #FF00FF, #00FFFF)`

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Orbitron** | 400-900 | Geometric, futuristic, ALL CAPS |
| Body/Code | **Share Tech Mono** | 400 | Terminal-like monospace |

- Hero: `text-5xl` to `text-9xl` (80-128px)
- Text glow effects mandatory on headlines

## Border Radius

- Primary: `rounded-none` (0px) — sharp geometric edges
- `rounded-full` for circles only
- No soft rounding

## Shadows (Neon Glow)

```css
/* Magenta glow */
box-shadow: 0 0 10px #FF00FF, 0 0 20px rgba(255, 0, 255, 0.3);

/* Cyan glow */
box-shadow: 0 0 20px rgba(0, 255, 255, 0.2);

/* Hover: 2-3x intensity + color inversion */
box-shadow: 0 0 30px #FF00FF, 0 0 60px rgba(255, 0, 255, 0.5);
```

## Component Patterns

### Buttons
- Aggressive `-skew-x-12` transform
- Inner content un-skewed (`skew-x-12`)
- Neon border glow
- Hover: glow amplifies 2-3x, background fills
- ALL CAPS, Orbitron font

### Cards
- Terminal/window chrome: colored control dots (red, yellow, green)
- Deep purple bg with glass effect
- Dual-border: cyan top + pink sides
- Hover: `-translate-y-2` + glow intensifies

### Inputs
- Dark bg, neon border on focus
- Monospace font
- Glow on focus state

## CRT / Scanline Effects

```css
/* Scanline overlay (apply to body::after) */
.scanlines::after {
  content: '';
  position: fixed;
  inset: 0;
  background: repeating-linear-gradient(
    0deg, rgba(0,0,0,0.1) 0px, rgba(0,0,0,0.1) 1px,
    transparent 1px, transparent 2px
  );
  pointer-events: none;
  z-index: 9999;
}

/* Chromatic aberration on text */
.chromatic {
  text-shadow: -2px 0 #FF00FF, 2px 0 #00FFFF;
}
```

## Animation

- Duration: 200ms, `ease-linear`
- Buttons: aggressive skew transforms
- Cards: lift + glow amplification
- Hover: 2-3x glow intensity + color inversion
- Background: perspective grid animation

## Signature Elements

1. **Aggressive skewing** — `-skew-x-12` on buttons/badges
2. **Global CRT scanlines** overlay
3. **RGB chromatic aberration** on text
4. **Perspective grid backgrounds** (CSS transforms)
5. **Gradient text fills** on hero headlines
6. **Rotating icon containers** — `rotate-45` diamond shapes
7. **Terminal window chrome** with colored control dots
8. **Massive blurred sun** — 600px diameter, `blur-[100px]`, ~20% opacity
9. **IRC-style testimonials** — `<username>` formatting
10. **Glow amplification** on hover (2-3x + color inversion)
11. **Alternating timeline layout**

## Anti-Patterns

- No warm/organic aesthetics
- No serif fonts
- No subtle/muted tones
- No soft shadows (neon glow only)
- No standard rounded buttons (skew them)
- No missing CRT/scanline effects
