# Academia (Classical)

> "Scholarly gravitas meets timeless elegance." Evokes prestigious university libraries and Victorian scholarship.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Deep Mahogany | `#1C1714` | Primary background |
| Aged Oak | `#251E19` | Surface/cards |
| Antique Parchment | `#E8DFD4` | Primary text |
| Polished Brass | `#C9A962` | ALL interactive elements |
| Library Crimson | `#8B2635` | Special emphasis only |

Dark, warm, aged palette. Brass is the primary accent for all interactions.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Cormorant Garamond** | 400-700 | High-contrast serif |
| Body | **Crimson Pro** | 400-500 | Book-style readability |
| Labels/Display | **Cinzel** | 400-700 | All-caps, engraved appearance |

- Hero: `text-5xl` to `text-7xl`
- Body: `text-base` to `text-lg`, generous `leading-relaxed`
- Labels: Cinzel, uppercase, tracked

## Border Radius

- Cards: minimal rounding or 0px
- Buttons: 0px to 4px
- Special: arch-topped images with `border-radius: 40% 40% 0 0 / 20% 20% 0 0`

## Shadows

- Warm, deep shadows: `rgba(28, 23, 20, 0.3)` to `rgba(28, 23, 20, 0.5)`
- Hover: shadow deepens
- Gold-tinted glow on interactive elements

## Component Patterns

### Buttons
- Brass background (`#C9A962`), dark text
- Uppercase Cinzel font
- Hover: brightness increase, subtle glow
- No rounded corners — rectangular

### Cards
- Aged oak background (`#251E19`)
- Subtle warm border
- Corner flourishes as decorative brackets

### Images
- Arch-topped: `border-radius: 40% 40% 0 0 / 20% 20% 0 0`
- Default sepia filter
- Hover: transition to full color

## Signature Elements

1. **Arch-topped images** — cathedral window shape via CSS border-radius
2. **Sepia-to-color transitions** on image hover
3. **Roman numeral sections** — "Volume I", "Volume II" in Cinzel
4. **Drop caps** — brass-colored Cinzel at paragraph starts
5. **Corner flourishes** — brass bracket decorations framing content
6. **Ornate dividers** — gradient lines with centered decorative glyphs
7. **Wax seal badges** — circular crimson with radial gradient depth
8. **Engraved text effects** — dual text-shadow creating pressed-metal look

## Textures

- Paper grain: subtle noise overlay
- Vignette: radial gradient darkening edges
- Wood grain patterns on surfaces (optional)

## Animation

- Slow, dignified transitions: 400-600ms
- `ease-out` easing
- Subtle hover effects — brightness shifts, not movement
- Image color transitions: 800-1000ms

## Anti-Patterns

- **Never use sans-serif** fonts
- No bright/vibrant colors
- No sharp/cold geometry
- No cold tones (blue, grey)
- No pure black or pure white
- No playful animations
- Must feel like an authentic library, not a generic dark theme

## Accessibility

- 8.5:1 contrast minimum (parchment on mahogany)
- Visible brass focus rings
- Semantic HTML throughout
- Respects `prefers-reduced-motion`
