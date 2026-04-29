# Brio Water — Agent Brief

Fast agent-safe brief. Read this first. Everything else expands on it.

## Core Identity

Brio Water Technology, Inc. makes clean water dispensers, filtration systems, and ice machines for homes, offices, and commercial spaces. Based in Southern California. Taglines: **"Feel Good About Your Water"** / **"Life Runs on Brio"**.

Design character: bright, clean, and confident. Primary cyan blue carries the brand. White surfaces dominate. Never cluttered.

## Color System

| Role | Token | Hex | Pantone |
|---|---|---|---|
| Primary blue | `--color-blue` | `#00A3E0` | BW 299C |
| Light blue | `--color-blue-light` | `#90C6EA` | BW 2905C |
| Deep navy | `--color-navy` | `#004D7A` | BW 7693C |
| Near-black text | `--color-charcoal` | `#24282B` | BW 426C |
| Secondary text | `--color-gray` | `#9EA1A2` | BW 422C |
| Backgrounds / borders | `--color-gray-light` | `#E4E1E5` | BW 663C |
| Default surface | `--color-white` | `#FFFFFF` | — |

**Critical rule:** Never use more than **2 highlight hues** in a single composition. Primary blue + one accent only.

## Typography

**Centura No 2** — the only brand typeface. Weights: Light, Book, Medium, Bold.
- Self-hosted woff2 files required (not on Google Fonts)
- Fallback stack: `Nunito, Poppins, system-ui, sans-serif`
- Labels: uppercase, 0.08em letter-spacing

## Non-Negotiables

- `#00A3E0` is the only primary blue — do not substitute with similar blues
- All labels uppercase with letter-spacing (brand voice is clean and structured)
- Buttons: rounded (`--radius-l`) with solid blue primary; white ghost with blue border
- White or `#F0F8FD` (ultra-light blue tint) for all default surfaces — never gray-heavy
- Shadow tints use brand blue (`rgba(0, 163, 224, …)`) — not generic black shadows
- Logo always in `#00A3E0` (color) or `#9EA1A2` gray (monochrome) — no other colors

## Authority Order

Tokens → this brief → AGENT_SKILLS.md → PRODUCT_UI.md → VOICE.md → BRAND.md
