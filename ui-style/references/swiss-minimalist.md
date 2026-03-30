# Swiss Minimalist (International Typographic Style)

> "Objectivity over Subjectivity: The design must recede to let the content speak." Rejects personal expression in favor of universal clarity, mathematical precision, and logical structure.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FFFFFF` | Primary canvas |
| Foreground | `#000000` | Text, borders, structure |
| Muted | `#F2F2F2` | Secondary backgrounds |
| Accent | `#FF3000` | Swiss Red — CTAs, critical emphasis only |
| Border | `#000000` | Structural definition |

Pure 4-color palette: white, black, gray, red. Nothing else permitted.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| All text | **Inter** | 400-900 | (Helvetica/Akzidenz-Grotesk fallbacks) |

- Headlines: weight 900 (Black) or 700 (Bold), UPPERCASE, `tracking-tighter`
- Body: weight 400/500, flush-left ragged-right
- Labels: `tracking-widest`, uppercase, in Swiss Red
- Scale: `text-6xl` (mobile) to `text-9xl` / `text-[10rem]` (desktop)

## Border Radius

**`0px` strictly.** No rounding anywhere.

## Shadows

**None.** Depth comes from pattern, grid structure, and contrast — never shadow.

## Borders

- `border-2` to `border-4`, always black
- Used as structural dividers, not decoration
- 4px black on desktop and mobile

## Spacing

- Standard padding: `p-8`
- Generous: `p-12`
- Hero sections: `p-24`
- Grid: 24x24px base unit

## Textures (CSS Patterns)

```css
/* Grid pattern */
background-image: repeating-linear-gradient(0deg, rgba(0,0,0,0.03) 0 1px, transparent 1px 24px),
                  repeating-linear-gradient(90deg, rgba(0,0,0,0.03) 0 1px, transparent 1px 24px);

/* Dot matrix */
background-image: radial-gradient(circle, rgba(0,0,0,0.04) 1px, transparent 1px);
background-size: 16px 16px;

/* Diagonal lines */
background-image: repeating-linear-gradient(45deg, rgba(0,0,0,0.02) 0 1px, transparent 1px 10px);

/* Noise overlay */
/* SVG fractal noise at 1.5% opacity */
```

## Component Patterns

### Buttons
- Rectangular `rounded-none`, black bg, white text
- UPPERCASE, bold, `tracking-wide`
- Hover: color inversion (white bg, black text) or switch to `#FF3000`
- No shadows, no radius

### Cards
- `border-black` 2-4px, white or `#F2F2F2` bg
- Hover: full color inversion (black bg, white text)
- Sharp corners, structural borders

### Inputs
- Underlined (`border-b`) or thick rectangular box
- Focus: sharp border change to Swiss Red
- Minimal styling — content-focused

### Icons (lucide-react)
- Functional, not decorative
- Rotate on hover (plus: 90deg, arrows: -45deg to 0deg)

## Layout

- Asymmetric grids: 8:4, 7:5, 5:7 ratios
- Strict left alignment
- 4px black dividers between sections
- Numbered section prefixes: "01. System", "02. Method" — in red

## Animation

- Instant, mechanical, snappy
- 150-200ms, `ease-out` or `ease-linear`
- Color snap (no fade — instant switch)
- Scale 1.0 to 1.05 on stats
- Nav links: vertical slide + color change

## Signature Elements

1. Massive typography as the visual centerpiece
2. Visible 4px grid borders / structural lines
3. Numbered sections in red ("01.", "02.")
4. Geometric abstraction (Bauhaus-inspired shapes)
5. Pattern layering (grid, dots, diagonals, noise)
6. Flush-left type alignment
7. Color inversion on hover
8. Functional-only red accent
9. Zero rounded corners anywhere
10. Focus ring: `ring-2 ring-[#FF3000] ring-offset-2`

## Anti-Patterns

- No rounded corners
- No shadows of any kind
- No decorative elements (every element must serve content)
- No multiple accent colors
- No centered text (flush-left always)
- No playful or organic shapes
