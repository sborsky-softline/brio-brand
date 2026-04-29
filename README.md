# brio-brand

Canonical design and build system for Brio Water branded products and marketing surfaces.

## Quick Start

1. License and self-host **Centura No 2** woff2 files in `/fonts/`
2. Import `tokens/tokens.css` for all CSS custom properties
3. Read `AGENT_BRIEF.md` for fast brand lookup
4. Copy component recipes from `AGENT_SKILLS.md`

## Structure

```
brio-brand/
├── .agents/skills/brio-brand/  ← Agent skill (agentskills.io format)
├── tokens/                      ← colors.json, typography.json, spacing.json, tokens.css
├── scss/                        ← globals.scss, _variables.scss
├── voice/                       ← VOICE.md (writing system)
├── assets/svgs/                 ← Logo files (add here)
├── AGENT_BRIEF.md               ← Fast reference — read first
├── AGENT_SKILLS.md              ← Copy-paste component recipes
├── BRAND.md                     ← Full design rationale
└── PRODUCT_UI.md                ← E-commerce patterns and page anatomy
```

## Authority Order

`tokens/tokens.css` → `AGENT_BRIEF.md` → `AGENT_SKILLS.md` → `PRODUCT_UI.md` → `voice/VOICE.md` → `BRAND.md`

## Font Note

Centura No 2 is a licensed typeface. Obtain a license before production use.
Fallback stack: `Nunito, Poppins, system-ui, sans-serif`
