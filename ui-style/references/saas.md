# SaaS

> "Clarity through structure, character through bold detail" — minimalism that makes a statement.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FFFFFF` | Primary canvas |
| Foreground | `#000000` | Primary text |
| Muted BG | `#F5F5F5` | Secondary surfaces |
| Muted FG | `#737373` | Secondary text |
| Accent Start | `#0052FF` | Electric blue gradient start |
| Accent End | `#4D7CFF` | Electric blue gradient end |
| Border | `#E5E5E5` | Subtle borders |

- Warm near-monochrome palette with electric blue gradient accent used sparingly but with maximum impact on CTAs, highlights, and accent elements
- Inverted contrast sections (dark background with light text) for visual rhythm

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| Headings | **Calistoga** | 400 | Warm, characterful serif |
| Body / UI | **Inter** | 400-600 | Clean sans-serif |
| Technical labels | **JetBrains Mono** | 400-500 | Monospace for data/stats |

- Hero: `text-5xl` to `text-7xl`, tight leading
- Body: `text-base` to `text-lg`, relaxed leading
- Labels: uppercase, `tracking-wide`, small text

## Border Radius

- Buttons: `rounded-lg` to `rounded-xl`
- Cards: `rounded-xl` to `rounded-2xl`
- Badges: `rounded-full`
- Inputs: `rounded-lg`

## Shadows

- Cards: `shadow-sm` base, `shadow-md` on hover with subtle lift
- Accent-tinted shadows on key elements: `shadow-[0_4px_14px_rgba(0,82,255,0.15)]`
- Layered depth through multiple shadow layers

## Spacing

- Generous section whitespace: `py-28` to `py-44`
- Component padding: `p-6` to `p-8`
- Container: `max-w-6xl` centered

## Component Patterns

### Buttons
- Primary: gradient background (`bg-gradient-to-r from-[#0052FF] to-[#4D7CFF]`), white text, lift on hover
- Secondary: white background, border, accent text
- All buttons: `px-6 py-3`, `font-medium`, smooth transitions

### Cards
- White backgrounds, subtle borders, layered shadows
- Hover: slight lift (`-translate-y-1`) + shadow enhancement
- Clean internal spacing with clear hierarchy

### Section Labels
- Consistent badge pattern: accent-tinted background, pulsing dot indicator, accent border
- Format: `[● Label Text]` as section header

### Inputs
- Clean borders, generous padding
- Focus: accent border + accent ring
- Labels above, helper text below

## Animation

- Transitions: `duration-200` to `duration-300`
- Hover lift on cards and buttons: `-translate-y-1`
- Pulsing indicators on live elements
- Floating cards with subtle rotation
- Rotating accent rings as decoration
- Easing: `ease-out` for most interactions

## Signature Elements

1. Electric blue gradient accent (sparingly applied)
2. Inverted contrast sections (dark bg sections)
3. Animated depth elements (pulsing dots, floating cards, rotating rings)
4. Strategic asymmetry within minimalist structure
5. Dot patterns and radial glows as decoration
6. Section label badges with pulsing dot

## Anti-Patterns

- No heavy shadows or excessive depth
- No more than one accent color
- Don't overuse the gradient — it loses impact
- No playful or rounded aesthetics
- No decorative illustrations — structure IS the decoration
- No cramped spacing

## Tech Stack

Tailwind CSS + custom CSS properties, Framer Motion for animations, shadcn/ui component patterns.
