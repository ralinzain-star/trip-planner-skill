# Cyberpunk

> "High-Tech, Low-Life" — digital dystopia from 80s sci-fi and hacker culture.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#0a0a0f` | Deep void |
| Surface | `#111118` | Card surfaces |
| Foreground | `#E0E0E0` | Primary text |
| Primary | `#00ff88` | Electric green — primary accent |
| Secondary | `#ff00ff` | Hot magenta |
| Tertiary | `#00d4ff` | Cyan |
| Border | `#1a1a2e` | Dark border |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Orbitron** or **Share Tech Mono** | 400-700 | Futuristic, geometric |
| Body | **JetBrains Mono** or **Fira Code** | 400 | Monospace throughout |

- ALL UPPERCASE headings
- Extensively letter-spaced: `tracking-widest`
- Hero: `text-4xl` to `text-7xl`

## Border Radius

**No standard border-radius.** Use `clip-path` for chamfered/cut corners:

```css
/* Chamfered corner */
clip-path: polygon(
  12px 0%, calc(100% - 12px) 0%,
  100% 12px, 100% calc(100% - 12px),
  calc(100% - 12px) 100%, 12px 100%,
  0% calc(100% - 12px), 0% 12px
);
```

## Shadows (Neon Glow)

```css
/* Green glow */
box-shadow: 0 0 10px rgba(0, 255, 136, 0.3),
            0 0 20px rgba(0, 255, 136, 0.1),
            0 0 40px rgba(0, 255, 136, 0.05);

/* Magenta glow */
box-shadow: 0 0 10px rgba(255, 0, 255, 0.3),
            0 0 20px rgba(255, 0, 255, 0.1);

/* Cyan glow */
box-shadow: 0 0 10px rgba(0, 212, 255, 0.3),
            0 0 20px rgba(0, 212, 255, 0.1);
```

## Borders

- `border border-[#00ff88]/30` — glowing neon borders
- Borders glow on hover with increased opacity

## Spacing

- Section padding: `py-20` to `py-32`
- Card padding: `p-6`
- Container: `max-w-6xl`

## Component Patterns

### Buttons
- Chamfered cuts via `clip-path`
- Neon glow box-shadow
- Background: accent color or transparent with neon border
- Hover: glow intensifies, background fills
- ALL CAPS, monospace, letter-spaced

### Cards
- Terminal window style: title bar with traffic-light dots (red/yellow/green circles)
- OR holographic glassmorphic variant with backdrop-blur
- `clip-path` chamfered corners
- Neon border glow

### Inputs
- Prefixed with `>` prompt symbol
- Monospace font
- Neon border on focus
- Dark background

## Animation

- Chromatic aberration: RGB color splitting on hover
- Scanline overlays: repeating-linear-gradient for CRT texture
- Glitch effects: occasional text displacement
- Neon pulse: 2s glow oscillation
- Duration: 200-300ms for interactions

## Signature Elements (Non-Negotiable)

1. **Chromatic aberration** — RGB color splitting on text/images
2. **CRT scanline overlay** — horizontal lines across the screen
3. **Chamfered corners** via `clip-path` (NOT border-radius)
4. **Multi-layered neon glow** shadows
5. **Terminal aesthetic** — monospace everything
6. **Traffic-light dots** on card title bars
7. **Glitch effects** on hover
8. **ALL CAPS** with wide letter-spacing

## CRT Scanline CSS

```css
.scanlines::after {
  content: '';
  position: fixed;
  inset: 0;
  background: repeating-linear-gradient(
    0deg,
    rgba(0, 0, 0, 0.15) 0px,
    rgba(0, 0, 0, 0.15) 1px,
    transparent 1px,
    transparent 2px
  );
  pointer-events: none;
  z-index: 9999;
}
```

## Anti-Patterns

- No rounded corners (use clip-path chamfers)
- No warm colors (everything is cold/neon)
- No serif fonts
- No subtle/muted aesthetics
- No standard card/button shapes
