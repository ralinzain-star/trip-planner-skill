# Professional Serif (Editorial)

> "Typographic elegance through classical restraint." Timeless, warm, sophisticated, literary confidence. Draws from luxury publications and literary magazines.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FAFAF8` | Ivory canvas |
| Foreground | `#1A1A1A` | Rich black |
| Muted BG | `#F5F3F0` | Secondary surfaces |
| Muted FG | `#6B6B6B` | Warm gray text |
| Accent | `#B8860B` | Burnished gold |
| Accent Secondary | `#D4A84B` | Lighter gold |
| Border | `#E8E4DF` | Warm border |

Single accent: burnished gold. Nothing else.

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headlines | **Playfair Display** | 400-700 | Serif |
| Body/UI | **Source Sans 3** | 400-600 | Sans-serif |
| Monospace | **IBM Plex Mono** | 400-500 | Technical |

- Hero: 4.5rem (72px), `tracking-[-0.02em]`
- Section labels: 12px IBM Plex Mono, weight 500, `tracking-[0.15em]`, uppercase
- Body: `leading-[1.75]` — generous line-height

## Border Radius

- Buttons: 6px
- Cards: 8px
- Minimal rounding — not sharp, not round

## Shadows

```css
/* Small */
box-shadow: 0 1px 2px rgba(26, 26, 26, 0.04);

/* Medium */
box-shadow: 0 4px 12px rgba(26, 26, 26, 0.06);

/* Large */
box-shadow: 0 8px 24px rgba(26, 26, 26, 0.08);
```

Subtle, warm-tinted — never heavy.

## Borders

- Thin: `1px solid #E8E4DF`
- Accent: `1px solid #B8860B` (gold)
- Section dividers: horizontal lines flanking uppercase labels

## Spacing

- Section padding: `py-32` to `py-44`
- Container: `max-w-5xl` (64rem)
- Component padding: `p-8` to `p-10`
- Grid gaps: `gap-8` to `gap-12`
- Body line-height: 1.75

## Component Patterns

### Buttons
- Gold bg (`#B8860B`), white text
- 44px min height, 6px radius
- Hover: lighter gold (`#D4A84B`) + shadow enhance + `-translate-y-0.5`
- Secondary: transparent with gold border

### Cards
- White bg, 1px warm gray border, 8px radius
- Subtle shadow, increases on hover
- Optional: 2px gold top border accent
- No lift on hover — shadow deepens only

### Section Labels
- Format: `——— LABEL TEXT ———`
- Horizontal lines flanking uppercase text
- Gold text, `tracking-[0.15em]`, IBM Plex Mono

## Animation

- Restrained, inevitable
- `transition-all duration-200 ease-out`
- Hover: subtle brightness changes (5-10%)
- No bouncing or overshooting
- Entrance: fade in 0.6s ease-out

## Signature Elements

1. **Oversized serif headlines** — 7xl hero with Playfair
2. **Thin horizontal rules** as section dividers
3. **Tracked uppercase small caps** — gold, monospace
4. **Burnished gold** as single accent throughout
5. **Generous whitespace** — py-32 to py-44
6. **Large serif display numbers** for statistics
7. **Decorative gold opening quotes** — oversized quotation marks
8. **Asymmetric columns** — content not centered
9. **Noise texture overlay** — 30% opacity grain
10. **Ambient glow** — 2% opacity accent circle background

## Anti-Patterns

- No vibrant/saturated colors
- No heavy shadows
- No playful animations
- No aggressive typography
- No cold/clinical tones
- No trendy/experimental effects
