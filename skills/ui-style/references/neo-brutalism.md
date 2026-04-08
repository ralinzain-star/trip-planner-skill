# Neo-Brutalism

> "Digital punk rebellion" against polished corporate design. Unapologetic visibility.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Canvas | `#FFFDF5` | Warm cream background |
| Ink | `#000000` | ALL text, ALL borders |
| Accent | `#FF6B6B` | Hot red — primary actions |
| Secondary | `#FFD93D` | Vivid yellow — highlights |
| Muted | `#C4B5FD` | Soft violet — decorative |
| White | `#FFFFFF` | High-contrast surfaces |

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| All text | **Space Grotesk** | 700-900 | Heavy weights only |

- Display: `text-8xl` to `text-9xl`
- Body: `text-base` to `text-lg`
- Labels: `text-sm`, ALL CAPS
- Treatment: uppercase emphasis, text-stroke outlines, tight leading
- Letter-spacing: `tracking-tight` for headlines

## Border Radius

**`rounded-none` (0px) everywhere.** Sharp corners are non-negotiable.

Only exception: `rounded-full` for small badges/pills.

## Shadows (Hard Offset — Zero Blur)

```css
/* Standard */
box-shadow: 4px 4px 0px 0px #000000;

/* Medium */
box-shadow: 8px 8px 0px 0px #000000;

/* Large */
box-shadow: 12px 12px 0px 0px #000000;

/* Extra Large */
box-shadow: 16px 16px 0px 0px #000000;
```

**ZERO blur on all shadows.** This is the defining visual characteristic.

## Borders

- `border-4` (4px) is the standard weight — thick and visible
- Always `border-black`
- Some elements use `border-2` minimum

## Spacing

- Section padding: `py-16` to `py-24`
- Card padding: `p-6` to `p-8`
- Container: `max-w-5xl`
- Generous gaps between elements

## Component Patterns

### Buttons
- Thick `border-4 border-black`
- Hard shadow: `shadow-[4px_4px_0px_0px_#000000]`
- Click "push down" effect: `active:translate-x-[4px] active:translate-y-[4px] active:shadow-none`
- Background in accent colors, bold text
- ALL CAPS, `font-bold`

### Cards
- White background, `border-4 border-black`
- Deep hard shadow: `shadow-[8px_8px_0px_0px_#000000]`
- Hover: lift with `-translate-y-2` + increased shadow
- Sharp corners only

### Inputs
- `border-4 border-black`, large bold text
- Focus: yellow background + shadow offset
- No soft focus rings — use border color change

## Animation

- Duration: `duration-150` max — snappy, not smooth
- Button press: translate to cover shadow offset
- Card hover: `-translate-y-2` lift
- No smooth easing — `ease-linear` or instant
- Sticker rotation: slight `rotate-1` to `-rotate-2` on decorative elements

## Signature Elements

1. **Hard shadows** — solid black offsets with ZERO blur
2. **Thick borders** — `border-4` minimum
3. **Sticker layering** — elements with slight rotation (`rotate-1`, `-rotate-2`) + absolute positioning
4. **Background textures** — halftone dots, grid patterns, noise overlays
5. **Zero border radius** — sharp corners everywhere
6. **Push-down buttons** — active state moves to cover shadow
7. **Warm cream canvas** — not pure white
8. **Heavy type** — bold/black weight Space Grotesk

## Anti-Patterns

- **NO blur effects** of any kind
- **NO opacity gradients** or subtle fades
- **NO mid-range rounding** (`rounded-md`, `rounded-lg`)
- **NO subtle grays** — only pure black or pure white
- **NO smooth animations** — everything is snappy
- **NO drop shadows with blur** — hard offsets only
- **NO thin borders** — minimum `border-2`, prefer `border-4`
