# Retro 90s

> Anti-modern maximalism celebrating 1995-1999 web aesthetics. "The ugliness IS the beauty." "Welcome to 1997."

## Color Palette (Pure RGB Values)

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#C0C0C0` | Windows 95 silver |
| Surface | `#FFFFFF` | White panels |
| Text | `#000000` | Black text |
| Links | `#0000FF` | Unvisited links |
| Visited Links | `#800080` | Visited links |
| Button Face | `#C0C0C0` | Button backgrounds |
| Highlight BG | `#000080` | Selected items |
| Highlight Text | `#FFFFFF` | Text on selection |

## Typography

| Role | Font | Notes |
|------|------|-------|
| System | **MS Sans Serif**, **Arial** | Default UI text |
| Headlines | **Arial Black** | Bold/Black weight |
| Code/Counter | **Courier New** | Monospace |

- Headings: BOLD or BLACK weight only — no thin/light fonts
- No font smoothing — pixel-perfect rendering
- Underline ALL links

## Border Radius

**`0px` everywhere.** No border-radius exists in this era.

## Borders (4-Value Bevel System)

The signature Windows 95 3D effect:

```css
/* Raised (default state) */
border-style: solid;
border-width: 2px;
border-color: #ffffff #808080 #808080 #ffffff;
box-shadow: inset 1px 1px 0 #dfdfdf, inset -1px -1px 0 #0a0a0a;

/* Pressed/inset */
border-color: #808080 #ffffff #ffffff #808080;
box-shadow: inset 1px 1px 0 #0a0a0a, inset -1px -1px 0 #dfdfdf;
```

## Shadows

Only the bevel system above. No soft shadows, no blur.

## Spacing

- Tight padding: `p-2` to `p-4`
- Minimal margins — pack content densely
- No generous whitespace — fill the viewport

## Component Patterns

### Buttons
- Beveled 3D border system (raised)
- Active: inverted bevel (pressed)
- Gray background (`#C0C0C0`)
- Uppercase or Title Case text
- `px-4 py-1`, compact

### Cards (Windows)
- Title bar: gradient blue (`#000080` to `#1084D0`)
- White content area with beveled frame
- Close/minimize/maximize buttons in title bar
- Visible scrollbars

### Inputs
- Inset beveled border (pressed)
- White background
- Courier New for text
- No placeholder text — use labels

### Tables
- Visible borders everywhere: `border-collapse: collapse; border: 2px solid`
- Alternating row colors optional
- Header: dark blue bg, white text

## Mandatory Visual Elements (10)

1. **Marquee scrolling text** (use `react-fast-marquee`)
2. **Animated rainbow text** cycling through colors
3. **Beveled 3D effects** on everything
4. **"Under Construction" badge** — pulsing, animated
5. **Groove-effect horizontal rules** — `border-style: groove`
6. **Hit counter** — green monospace on dark background
7. **Table-like grid layouts** with visible borders
8. **Windows 95 title bar gradients** on cards
9. **Decorative color squares grid**
10. **Yellow/black diagonal construction stripes**

## Animation

- Marquee scrolling: continuous, linear
- Rainbow text: cycling through `#FF0000, #FF7F00, #FFFF00, #00FF00, #0000FF, #4B0082, #9400D3`
- Blink tags: pulsing opacity
- Spinning/rotating decorative GIF-style elements
- No smooth easing — linear or step transitions

## Anti-Patterns

- **NO border-radius** — corners are always 90 degrees
- **NO soft shadows** — only bevel system
- **NO semi-transparent overlays**
- **NO thin/light fonts** — bold and black only
- **NO smooth easing** — linear or steps
- **NO removing link underlines**
- **NO attempting to "modernize"** the aesthetic
- **NO responsive design** (optional: minimal mobile adaptation)
