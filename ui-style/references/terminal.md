# Terminal CLI

> Cyber-Industrial, Hacker, System-Level aesthetic. "Brutally functional, high-contrast, and authentically retro."

## Color Palette (Dark Mode Only)

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#0a0a0a` | Deep black |
| Primary | `#33ff00` | Bright neon green |
| Secondary | `#ffb000` | Amber/orange |
| Muted | `#1f521f` | Dimmed green |
| Error | `#ff3333` | Bright red |
| Border | `#1f521f` | 1px dimmed green |

## Typography

**Monospace exclusively.** No other font families.

| Role | Font | Notes |
|------|------|-------|
| All text | **JetBrains Mono**, **Fira Code**, or **VT323** | Monospace only |

- Headers: ALL CAPS
- Body/Code: lowercase
- Modular grid-aligned sizing
- Text glow: `text-shadow: 0 0 5px rgba(51, 255, 0, 0.5)` (phosphor effect)

## Border Radius

**`0px` everywhere.** No rounding.

## Borders

- `1px solid` or `1px dashed` in muted green (`#1f521f`)
- ASCII-style decorative borders: `+--- TITLE ---+`

## Shadows

None. Only text-shadow glow effects.

## Spacing

- Strict character grid layout
- Monospace alignment
- Compact but readable

## Component Patterns

### Buttons
- Text in brackets: `[ INITIATE ]`, `[ DEPLOY ]`
- Green text on black
- Hover: inverted-video (green bg, black text)
- No padding decorations — just text

### Cards / Windows
- Black boxes with 1px green border
- Title bars: `+--- SYSTEM STATUS ---+`
- Content area below
- ASCII box-drawing characters for decoration

### Inputs
- Prompt-style: `user@acme:~$ ` prefix
- Blinking block cursor animation
- No focus ring — cursor blink is the indicator
- Green text on black bg

### Dividers
- ASCII: `----------------` or `================`
- No `<hr>` styling — literal dashes

### Status Indicators
- `[OK]` in green
- `[ERR]` in red
- `[WARN]` in amber

## Animation

- **Blink**: cursor blink (`_`) — 1s interval
- **Glitch**: subtle text offset (2px displacement, 100ms)
- **Typing**: character-by-character reveal
- **Progress bars**: ASCII `[||||||||||.....]`
- No smooth easing — step functions or linear

## Layout

- Strict character grid (resembles tmux/vim splits)
- Long lines wrap with backslash `\` on mobile
- Stack vertically on mobile, maintain monospace
- Panels side-by-side on desktop (terminal panes)

## Signature Elements

1. **Monospace supremacy** — every character on a grid
2. **Blinking cursor** (`_` or `█`)
3. **Shell metaphors** — `>`, `$`, `~`, `--help`, `[OK]`, `[ERR]`
4. **CRT scanline effect** overlay
5. **Phosphor text glow** — green text-shadow
6. **ASCII box drawing** for borders and decorations
7. **Prompt-style inputs** with `$` prefix
8. **Bracket notation** for buttons `[ ACTION ]`

## Anti-Patterns

- **NO non-monospace fonts**
- No rounded corners
- No gradients
- No images (ASCII art only if needed)
- No soft/subtle colors
- No traditional button/card styling
- No responsive breakpoints that break the grid
