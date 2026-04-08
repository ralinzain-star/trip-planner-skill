# Material Design 3 (Material You)

> "Personal, adaptive, and spirited" — organic shapes, tonal surfaces, and expressive color over rigid geometry.

## Color Palette (Light Mode)

| Token | Hex | Usage |
|-------|-----|-------|
| Background | `#FFFBFE` | Primary surface (never pure white) |
| Foreground | `#1C1B1F` | Default text |
| Primary | `#6750A4` | CTAs, focus, key interactions |
| On Primary | `#FFFFFF` | Text on primary |
| Secondary Container | `#E8DEF8` | Pills, chips, secondary containers |
| On Secondary Container | `#1D192B` | Text on secondary surfaces |
| Tertiary | `#7D5260` | Accent elements, FABs |
| Surface Container | `#F3EDF7` | Card backgrounds |
| Surface Container Low | `#E7E0EC` | Inputs, recessed surfaces |
| Outline | `#79747E` | Borders, dividers |
| On Surface Variant | `#49454F` | Secondary text, icons |

## Typography

| Role | Size | Weight | Tracking |
|------|------|--------|----------|
| Display Large | 56px | 400 | 0 |
| Headline Large | 48px | 400 | 0 |
| Headline Medium | 32px | 400 | 0 |
| Title Large | 24px | 500 | 0 |
| Body Large | 20px | 400 | 0 |
| Body Medium | 16px | 400 | 0 |
| Label Medium | 14px | 500 | 0.01em |
| Label Small | 12px | 500 | 0.01em |

Font: **Roboto** (400, 500, 700)

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| Extra Small | 8px | Small elements |
| Small | 12px | Chips, small cards |
| Medium | 16px | Cards, dialogs |
| Large | 24px | Large containers |
| Extra Large | 28px | Featured cards |
| Full | 9999px | All buttons (pill-shaped) |

- Inputs: top corners 12px, bottom 0px (`rounded-t-lg rounded-b-none`)

## Shadows (Elevation Levels)

| Level | Shadow | Usage |
|-------|--------|-------|
| 0 | none / `shadow-sm` | Default surface |
| 1 | `shadow-sm` | Cards at rest |
| 2 | `shadow-md` | Cards on hover |
| 3 | `shadow-lg` to `shadow-xl` | FABs, major sections |
| 4+ | Dialogs, modals | Elevated overlays |

## Component Patterns

### Buttons (ALL `rounded-full` pill-shaped)
- **Filled**: `bg-[#6750A4]` text-white
- **Tonal**: `bg-[#E8DEF8]` text-[#1D192B]
- **Outlined**: transparent, `border border-[#79747E]`
- **Text/Ghost**: transparent, no border
- **FAB**: `bg-[#7D5260]`, 56x56px, `rounded-[16px]`
- All: `active:scale-95` tactile feedback

### Cards
- `bg-[#F3EDF7]`, `rounded-3xl` (24px)
- `shadow-sm` default → `shadow-md` on hover
- `hover:scale-[1.02]`

### Inputs (Filled Text Field)
- Height: 56px
- Top radius 12px, bottom square
- 2px bottom border: `#79747E` rest, `#6750A4` focus
- Background: `#E7E0EC`

### Chips
- `rounded-full`, `border border-[#79747E]`
- Selected: filled with secondary container color

## State Layer System

| State | Solid | Transparent |
|-------|-------|-------------|
| Hover | 90% opacity | primary at 10% |
| Active | 80% opacity | primary at 5% |
| Focus | — | primary at 5% |

## Animation

- Signature easing: `cubic-bezier(0.2, 0, 0, 1)` on ALL transitions
- Duration: 200-500ms range
- `active:scale-95` on buttons (tactile feedback)
- Cards: `hover:scale-[1.02]`

## Signature Elements

1. **Organic decorative shapes** — `rounded-[100px]` or `rounded-full`, `blur-3xl`, `mix-blend-multiply`, 10-30% opacity, partial off-canvas
2. **Pill-shaped buttons** — all buttons are `rounded-full`
3. **Tonal surfaces** — color hierarchies through surface tints, not borders
4. **Material easing** — `cubic-bezier(0.2, 0, 0, 1)` everywhere
5. **Tactile feedback** — `active:scale-95` on interactive elements

## Anti-Patterns

- No pure white backgrounds (use `#FFFBFE`)
- No rectangular buttons (always pill/rounded-full)
- No heavy drop shadows
- No color-shift hovers (use opacity overlays)
- No sharp corners on major containers
- No pure black text (use `#1C1B1F`)
- No flat inputs (always recessed with bottom border)
- No radius <16px on cards
- No missing organic blur shapes in background
