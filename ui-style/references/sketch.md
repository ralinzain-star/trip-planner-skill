# Sketch / Hand-Drawn

> "Authentic imperfection and human touch." Rejects clinical precision for organic, playful irregularity. Napkin diagrams and sticky notes.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#fdfbf7` | Warm paper |
| Foreground | `#2d2d2d` | Soft pencil black |
| Muted | `#e5e0d8` | Old paper/erased pencil |
| Accent Red | `#ff4d4d` | Correction marker |
| Accent Blue | `#2d5da1` | Ballpoint pen |
| Card | `#ffffff` | White base |
| Feature | `#fff9c4` | Post-it yellow |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Kalam** | 700 | Thick felt-tip marker |
| Body | **Patrick Hand** | 400 | Legible handwritten |

Handwritten fonts exclusively — no system/sans-serif fonts.

## Border Radius (Wobbly — The Defining Feature)

```css
/* Irregular hand-drawn border */
border-radius: 255px 15px 225px 15px / 15px 225px 15px 255px;

/* Alternative wobbly variants */
border-radius: 15px 255px 15px 225px / 225px 15px 255px 15px;
border-radius: 225px 15px 255px 15px / 15px 255px 15px 225px;
```

**NEVER use standard Tailwind `rounded-*` classes.** Every border must be irregular.

## Shadows (Hard Offset Only — No Blur)

```css
/* Standard */
box-shadow: 4px 4px 0px 0px #2d2d2d;

/* Emphasized */
box-shadow: 8px 8px 0px 0px #2d2d2d;

/* Hover (lift — reduced offset) */
box-shadow: 2px 2px 0px 0px #2d2d2d;

/* Active (pressed flat — no shadow) */
box-shadow: none;
```

## Borders

- `border-2 border-[#2d2d2d]` standard
- All with wobbly border-radius
- Dashed borders for annotations

## Background

```css
/* Dot-grid paper */
background-image: radial-gradient(#e5e0d8 1px, transparent 1px);
background-size: 24px 24px;
```

## Component Patterns

### Buttons
- Wobbly border-radius, `border-2`
- Hard offset shadow
- Active: `translate-x-[2px] translate-y-[2px]` + shadow disappears (pressed flat)
- Kalam font, bold

### Cards
- White bg, wobbly borders
- Hard offset shadow
- Hover: slight rotation (`rotate-1` or `-rotate-1`) + reduced shadow
- Post-it yellow variant for featured items

### Inputs
- Wobbly border, handwritten font
- Focus: border color change to blue (`#2d5da1`)
- Patrick Hand font for placeholder/value

## Decorative Elements

- **Tape strips**: rotated rectangles at card tops
- **Thumbtack pins**: circular dots with shadow
- **Speech bubbles**: wobbly border with pointer
- **Dashed arrows**: SVG hand-drawn arrow curves
- **Squiggly underlines**: wavy SVG lines

## Animation

- Fast, snappy: `duration-100`
- Small playful rotations: `rotate-1`, `-rotate-2`
- Button press: translate to cover shadow + shadow disappears
- No smooth/elegant transitions — playful and quick

## Signature Elements

1. **Irregular border-radius** — NO straight lines anywhere
2. **Hard offset shadows** (never blur)
3. **Handwritten fonts** exclusively (Kalam + Patrick Hand)
4. **Hand-drawn SVG decorations** — arrows, squiggles, underlines
5. **Paper effects** — tape strips, thumbtacks, speech bubbles
6. **Playful rotation** — elements break grid by 1-2 degrees
7. **Button "press flat"** — shadow disappears on active
8. **Dot-grid paper background**
9. **Limited palette** — pencil blacks, paper whites, marker red, post-it yellow
10. **Hide decorative SVGs on mobile** for clean experience

## Anti-Patterns

- No straight/regular borders
- No system fonts
- No blur shadows
- No clinical precision
- No dark mode
- No complex animations
