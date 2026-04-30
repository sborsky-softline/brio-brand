# Fonts

The Brio brand typeface is wired up via `@font-face` blocks at the top of
`colors_and_type.css`. Files in this folder:

- `CentraNo-Hairline.ttf` (100)
- `CentraNo-Thin.ttf` (200)
- `CentraNo-Light.ttf` / `CentraNo-LightItalic.ttf` (300)
- `CentraNo-Book.ttf` / `CentraNo-BookItalic.ttf` (400) — default body
- `CentraNo-Medium.ttf` / `CentraNo-MediumItalic.ttf` (500)
- `CentraNo-Bold.ttf` / `CentraNo-BoldItalic.ttf` (700)
- `CentraNo-Extrabold.ttf` (800)
- `CentraNo-Black.ttf` (900)

## Naming note (flagged for the user)

The brand docs reference **"Centura No 2"** as the typeface name. The font
files attached are named **"Centra No"** (no `u`, no `2`). They appear to be
the correct family — geometric, rounded, full weight range — but the name
mismatch is worth confirming.

The CSS `@font-face` declarations alias these as `'Centura No 2'` so all
existing Brio code/tokens resolve cleanly. If the brand owner wants the
canonical name updated to `'Centra No'`, do a project-wide find/replace.
