# Modern Dark

> Linear-inspired — "precision, depth, and fluidity" with cinematic lighting.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| Background (deepest) | `#020203` | Page background |
| Background (base) | `#050506` | Section backgrounds |
| Surface | `rgba(255,255,255,0.05)` | Card surfaces (translucent) |
| Surface Hover | `rgba(255,255,255,0.08)` | Hover states |
| Foreground | `#EDEDEF` | Primary text (not pure white) |
| Muted | `#8B8B8D` | Secondary text |
| Accent | `#5E6AD2` | Indigo — single accent color |
| Border | `rgba(255,255,255,0.08)` | Subtle borders |

- Single accent color (indigo) — never add more
- Layer translucency at 5-10% opacity for surfaces
- Never use pure black or pure white

## Typography

| Role | Font | Weight | Notes |
|------|------|--------|-------|
| All text | **Inter** or **Geist Sans** | 400-700 | Tight tracking on headlines |

- Hero: `text-4xl` mobile to `text-7xl`/`text-8xl` desktop
- Body: `text-base` to `text-lg`
- Gradient text fills: white-to-transparent and animated accent gradients on headlines

## Border Radius

- Cards: `rounded-xl` to `rounded-2xl`
- Buttons: `rounded-lg`
- Inputs: `rounded-lg`
- Badges: `rounded-full`

## Shadows (Three-Layer System)

1. **Border glow**: `border border-white/[0.08]`
2. **Diffuse shadow**: `shadow-[0_4px_24px_rgba(0,0,0,0.4)]`
3. **Accent glow** (on key elements): `shadow-[0_0_20px_rgba(94,106,210,0.15)]`

## Spacing

- Section padding: `py-24` to `py-32`
- Card padding: `p-6` to `p-8`
- Container: `max-w-6xl`
- 4px base unit

## Component Patterns

### Buttons
- Primary: accent background (`bg-[#5E6AD2]`), white text
- Ghost: transparent, `border border-white/10`, hover glow
- Hover: subtle brightness increase + accent glow
- `px-5 py-2.5`, `font-medium`

### Cards
- Translucent surface: `bg-white/[0.05]`, `backdrop-blur-sm`
- Subtle border: `border border-white/[0.08]`
- Hover: border brightens to `border-white/[0.15]`
- Asymmetric bento grid layouts with mixed column spans

### Inputs
- Dark surface background, subtle border
- Focus: accent border + accent glow
- Placeholder text in muted color

## Animation

- Duration: 200-300ms
- Easing: expo-out `cubic-bezier(0.16, 1, 0.3, 1)`
- Hover transforms: 4-8px maximum movement
- Staggered entrance animations: 0.08s intervals
- Multi-layer animated gradient blobs: 900-1400px diameter, 8-10s float cycles
- Mouse-tracking radial spotlight (300px diameter, 15% opacity)
- Scroll-linked parallax on hero content

## Signature Elements

1. **Animated gradient blobs** — large background elements, 8-10s float cycle
2. **Mouse-tracking spotlight** — radial gradient follows cursor
3. **Gradient text** — white-to-transparent on headlines
4. **Translucent surfaces** — glass-like cards with backdrop-blur
5. **Single indigo accent** — used consistently for all interactive elements
6. **Asymmetric bento grids** — mixed column spans
7. **Staggered reveals** — entrance animations with slight delays

## Anti-Patterns

- No flat backgrounds (always layer with translucency)
- No pure black (`#000000`) or pure white (`#FFFFFF`)
- No uniform grids — use asymmetric bento layouts
- No bouncy animations (expo-out only)
- No missing glow effects on interactive elements
- No more than one accent color
- No heavy shadows (subtle glows instead)
