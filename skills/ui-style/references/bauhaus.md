# Bauhaus

> "Form follows function." Constructivist modernism. Geometric beauty and primary color theory. Interface as geometric composition.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#F0F0F0` | Off-white canvas |
| Foreground | `#121212` | Stark black |
| Primary Red | `#D02020` | Bauhaus red |
| Primary Blue | `#1040C0` | Bauhaus blue |
| Primary Yellow | `#F0C020` | Bauhaus yellow |
| Muted | `#E0E0E0` | Secondary gray |

Strictly: black, white, gray, plus three primaries. No other colors.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| All text | **Outfit** | 400-900 | Single geometric sans |

- Headlines: weight 900 (Black), UPPERCASE, `tracking-tighter`, `leading-[0.9]`
- Display: `text-4xl` mobile to `text-8xl` desktop
- Body: weight 400-500

## Border Radius (Binary Only)

**Only two options:**
- `rounded-none` (0px) — squares/rectangles
- `rounded-full` (9999px) — perfect circles

No intermediate values. No `rounded-md`, `rounded-lg`, etc.

## Shadows (Hard Offset, Black Only)

```css
/* Small */
box-shadow: 3px 3px 0px 0px #121212;

/* Medium */
box-shadow: 6px 6px 0px 0px #121212;

/* Large */
box-shadow: 8px 8px 0px 0px #121212;

/* Active (pressed) */
box-shadow: none;
```

## Borders

- Standard: `border-2 border-[#121212]`
- Major divisions: `border-4`
- Always black

## Spacing

- Section padding: `py-16` to `py-24`
- Card padding: `p-6` to `p-8`
- Container: `max-w-6xl`

## Component Patterns

### Buttons
- Primary color bg, black border, sharp corners
- Active: `translate-y-[2px]` + shadow disappears
- Bold uppercase text
- Hard shadow

### Cards
- White or colored bg, `border-2 border-black`
- Hard shadow
- Hover: `-translate-y-1`
- Sharp corners (never rounded)

### Images
- Default: `grayscale`
- Hover: `grayscale-0` reveal full color
- Alternating: round crops (circle) and square crops

## Color-Blocked Sections

Each section gets a primary color treatment:
- Hero: Blue background
- Stats: Yellow background
- Blog: Blue background
- Benefits: Red background
- CTA: Yellow background
- Footer: Black background

Rotate through primaries for visual rhythm.

## Animation

- Button press: `translate-y-[2px]` + shadow-none
- Card hover: `-translate-y-1`
- Duration: 200-300ms, `ease-out`
- Mechanical, snappy feel
- Image: grayscale → color on hover

## Signature Elements

1. **Color-blocked sections** — each section assigned a primary
2. **Geometric logo** — circle + square + triangle in primary colors
3. **Overlapping geometric compositions** — layered shapes
4. **45-degree rotations** on every 3rd decorative shape
5. **Corner decorations** — 8-16px geometric shapes in rotating primaries
6. **Alternating image crops** — round and square
7. **Asymmetric balance** with overlapping elements
8. **Section dividers** — `border-b-4 border-black`
9. **Binary radius** — only 0px or 9999px
10. **Primary-only palette** — red, blue, yellow, black, white

## Anti-Patterns

- No intermediate border-radius values
- No non-primary colors
- No gradients
- No soft shadows (hard offset only)
- No organic/irregular shapes
- No decorative fonts
