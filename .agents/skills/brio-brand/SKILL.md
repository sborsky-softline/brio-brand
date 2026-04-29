# Brio Water Brand System

Brio Water Technology, Inc. makes water dispensers, filtration systems, and ice machines for homes and businesses. This skill gives you everything needed to build Brio-branded surfaces correctly.

## Core Design Elements

**Colors:** Primary cyan blue (`#00A3E0`, Pantone BW 299C) anchors the brand. Secondary light blue (`#90C6EA`) for accents and hover states. Deep navy (`#004D7A`) for dark feature sections. Charcoal (`#24282B`) for all text. **Critical rule: never use more than 2 highlight hues in a single composition.**

**Typography:** Centura No 2 (Light, Book, Medium, Bold) is the exclusive brand typeface — licensed, self-hosted, not on Google Fonts. All labels are uppercase with `0.08em` letter-spacing. Fallback: `Nunito, Poppins, system-ui, sans-serif`.

**Signature Patterns:** Uppercase labeled buttons with 1.6rem radius. Product cards with blue-tinted shadows and hover lift. Dark navy feature sections. Trust/stat bars in `#E4E1E5` gray-light. Ultra-light `#F0F8FD` tint for alternating sections.

## Key Principles

- `#00A3E0` is the primary blue — never substitute; it matches Pantone BW 299C exactly
- Never use `#00A3E0` as a large full-section background fill — CTAs, text, and accents only
- All button and label text is uppercase, Centura No 2 Bold
- Shadows are always blue-tinted: `rgba(0, 163, 224, …)` not black
- Voice: clean, confident, benefit-first — "99% of contaminants removed" not "advanced filtration technology"

## Reference Documents

| File | Use |
|---|---|
| `AGENT_BRIEF.md` | Quick token + rule lookup |
| `AGENT_SKILLS.md` | Copy-paste component recipes |
| `BRAND.md` | Full design rationale, logo rules, don'ts |
| `PRODUCT_UI.md` | Page anatomy, e-commerce patterns, responsive grid |
| `voice/VOICE.md` | Writing formulas, product copy rules, banned words |
| `tokens/tokens.css` | All CSS custom properties |
| `scss/globals.scss` | Base styles and component classes |
