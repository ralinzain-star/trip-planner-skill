# Art Deco

> "The Roaring Twenties — jazz, prosperity, unbridled optimism." Opulence through geometric precision. "The Great Gatsby" meets "Metropolis."

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#0A0A0A` | Obsidian black |
| Foreground | `#F2F0E4` | Champagne cream |
| Card | `#141414` | Rich charcoal |
| Primary Gold | `#D4AF37` | Metallic gold — primary accent |
| Secondary | `#1E3D59` | Midnight blue |
| Muted | `#888888` | Pewter |
| Lighter Gold | `#F2E8C4` | Hover brightness |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Display | **Marcellus** or **Italiana** | 400 | Classical serif |
| Body | **Josefin Sans** | 300-400 | Geometric vintage sans |

- ALL headings: UPPERCASE with `tracking-widest` (0.2em)
- H1: `text-6xl` to `text-7xl`
- Body: `text-base` to `text-lg`

## Border Radius

**`0px` strict.** 2px rare exception. Sharp geometric edges.

For stepped corners, use `clip-path`:
```css
/* Stepped corner (Art Deco signature) */
clip-path: polygon(0 0, calc(100% - 16px) 0, 100% 16px, 100% 100%, 16px 100%, 0 calc(100% - 16px));
```

## Shadows (Glow-Based, Not Drop)

```css
/* Standard gold glow */
box-shadow: 0 0 15px rgba(212, 175, 55, 0.2);

/* Hover intensified */
box-shadow: 0 0 20px rgba(212, 175, 55, 0.4);
```

Simulates neon/backlit 1920s signage — never traditional drop shadows.

## Borders

- `1px solid` gold or champagne
- Decorative double borders on featured elements
- L-bracket corner decorations

## Component Patterns

### Buttons
- Gold border, transparent bg
- Hover: gold bg fills, champagne text
- UPPERCASE, `tracking-widest`, Josefin Sans
- Sharp corners, gold glow on hover

### Cards
- Charcoal bg, gold border
- **Stepped corner L-bracket decorations** at corners
- Hover: `-translate-y-2` + gold glow, 500ms
- **Double-frame images**: outer gold + inner dark border

### Roman Numerals
- Use I, II, III, IV instead of 1, 2, 3, 4
- Marcellus font, gold color
- Section numbering and step indicators

## Decorative Patterns

```css
/* Diagonal crosshatch (apply to sections) */
background-image: repeating-linear-gradient(
  45deg, rgba(212,175,55,0.03) 0 1px, transparent 1px 20px
), repeating-linear-gradient(
  -45deg, rgba(212,175,55,0.03) 0 1px, transparent 1px 20px
);

/* Sunburst radial */
background: radial-gradient(circle at center, rgba(212,175,55,0.1) 0%, transparent 70%);
```

## Animation

- Standard: 300ms `ease-out`
- Theatrical: 500ms `ease-in-out`
- Card hover: `-translate-y-2`, 500ms
- Mechanical, theatrical — like elevator doors
- Gold glow transitions

## Signature Elements

1. **Diagonal crosshatch background** — 45-degree gold lines, 3-5% opacity
2. **Rotated diamond containers** — `rotate-45` with counter-rotated content
3. **Roman numerals** — I, II, III instead of 1, 2, 3
4. **Stepped corner L-bracket decorations** on cards
5. **Double-frame images** — outer gold + inner dark border
6. **Sunburst radial gradients** — gold, 10-20% opacity
7. **Decorative gold divider lines** — `h-px w-24`
8. **Vertical architectural divider lines**
9. **Glow effects** over drop shadows
10. **All-caps display** with extreme tracking (0.2em)

## Anti-Patterns

- No rounded corners
- No modern/clean aesthetics
- No bright/saturated colors
- No sans-serif headings
- No standard drop shadows (glow only)
- No informal typography
