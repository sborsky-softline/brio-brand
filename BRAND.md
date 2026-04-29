# Brio Water — Brand System

Full design and voice reference. Use AGENT_BRIEF.md for fast lookups; come here for rationale.

---

## Who We Are

Brio Water Technology, Inc. designs and sells water dispensers, bottleless coolers, filtration systems, ice machines, and accessories for residential and commercial use. Based in Southern California.

**What we make:** Clean water, beautifully delivered.
**How we think:** Design-forward, wellness-driven, sustainability-minded.
**Who we serve:** Homeowners, offices, gyms, businesses — anyone who wants better water without the burden of bottles.

---

## Color System

### Complete Palette

| Name | Hex | Pantone | Use |
|---|---|---|---|
| Blue | `#00A3E0` | BW 299C | Logo, primary CTAs, headings, links, key accents |
| Blue Light | `#90C6EA` | BW 2905C | Secondary accents, hover states, tinted backgrounds |
| Navy | `#004D7A` | BW 7693C | Dark sections, footer accents, deep overlays |
| Charcoal | `#24282B` | BW 426C | Body text, footer background |
| Gray | `#9EA1A2` | BW 422C | Secondary text, metadata, monochrome logo |
| Gray Light | `#E4E1E5` | BW 663C | Page backgrounds, borders, dividers, cards |
| White | `#FFFFFF` | — | Default surface, cards, overlays |

### The 2-Hue Rule

Per the official Brio brand guide: **never use more than 2 highlight hues in a single composition.** In practice:
- Most layouts: `#00A3E0` (primary) + white
- Accented layouts: `#00A3E0` + `#90C6EA`
- Dark sections: `#004D7A` + `#00A3E0`

Charcoal, gray, and gray-light are neutrals and don't count toward the 2-hue limit.

### Section Tint
For alternating content sections use `#F0F8FD` — an ultra-light blue tint that stays on-brand without competing with `#00A3E0`.

---

## Typography

### Font

**Centura No 2** is the Brio typeface across all weights: Light, Book, Medium, Bold.

- **Not available on Google Fonts** — must be licensed and self-hosted
- Self-host as woff2 files in `/fonts/`
- Fallback: `Nunito, Poppins, system-ui, sans-serif`
- Character: geometric, rounded, approachable — matches the water drop logo's clean curves

### Weights in Use

| Weight | Use |
|---|---|
| Light | Large display text, hero subtitles |
| Book | Body copy, descriptions, all default text |
| Medium | H2–H4, nav items, card titles |
| Bold | H1, hero headlines, CTAs, badges |

### Type Scale

| Name | Size | Weight | Notes |
|---|---|---|---|
| Hero / H1 | `clamp(3.2rem, 6vw, 7.2rem)` | Bold | Page heroes |
| H2 | `clamp(2.4rem, 3.5vw, 4.4rem)` | Medium | Section headings |
| H3 | `clamp(2rem, 2.5vw, 3rem)` | Medium | Sub-sections |
| H4 | `clamp(1.8rem, 2vw, 2.4rem)` | Medium | Card titles |
| Body L | `2rem` | Book | Intro paragraphs, hero subtext |
| Body | `1.7rem` | Book | Default copy |
| Body S | `1.5rem` | Book | Captions, metadata |
| Label | `1.3rem` | Medium | Uppercase + `0.08em` letter-spacing — tags, badges, nav |

---

## UI Patterns

### Hero / Banner
- White or `#F0F8FD` background
- H1 in `#00A3E0` blue (Centura No 2 Bold)
- Subtext in charcoal, Body L
- Product image right-aligned (or full bleed on lifestyle campaigns)
- Primary CTA: solid blue pill button

### Product Cards
- White background, `--radius-l` corners (1.6rem)
- `--shadow-card` on default, `--shadow-hover` on hover
- Product image top (square, object-fit: contain on white)
- Product name: H4, charcoal
- Price: Body L, charcoal; sale price in `#00A3E0`
- Badges: "NEW", "EXCLUSIVE", "50% OFF" — uppercase label style, blue bg, white text
- "Quick Add" button appears on hover

### Buttons

**Primary (solid blue):**
```css
background: #00A3E0;
color: #FFFFFF;
border-radius: 1.6rem;
padding: 1.2rem 2.8rem;
font-family: 'Centura No 2';
font-weight: 700;
text-transform: uppercase;
letter-spacing: 0.06em;
```

**Secondary (ghost):**
```css
background: transparent;
color: #00A3E0;
border: 2px solid #00A3E0;
border-radius: 1.6rem;
```

**Dark (on dark sections):**
```css
background: #FFFFFF;
color: #004D7A;
border-radius: 1.6rem;
```

### Navigation
- White header, sticky
- Logo left; mega-menu center; cart/search/account icons right
- Nav items: Centura No 2 Medium, uppercase label style
- Mega-menu: product category images + subcategory text links

### Dark / Navy Sections
Used for callouts, feature highlights, and promotional banners:
- Background: `#004D7A`
- Text: white
- Accent: `#00A3E0` (or `#90C6EA` for secondary text)
- CTA: white button with navy text

---

## Logo

**Mark:** A water droplet above the "i" in "Brio." The droplet contains an inner wave/swirl shape. Represents purity, flow, refreshment.

**Wordmark:** "Brio" in Centura No 2 Bold (custom-spaced).

**Color versions:**
- **Full color:** `#00A3E0` — use on white or very light backgrounds
- **Monochrome:** `#9EA1A2` — for grayscale contexts, embossing, co-branding
- **Reversed:** white — use on blue or dark navy backgrounds only

**Do not:** recolor the logo, add effects, use on busy photography without a white/dark backing, stretch or distort.

---

## Motion

- Hover transitions: `220ms cubic-bezier(0.16, 1, 0.3, 1)`
- Product card hover: lift + blue shadow
- Button hover: `opacity: 0.88` + `translateY(-1px)`
- Page-load: fade + translateY(16px → 0), 380ms, staggered
- Keep animations purposeful — this is a product/e-commerce brand, not a showcase site

---

## Don'ts

- Never use more than 2 highlight hues in one composition
- Never use `#000000` — use `--color-charcoal` (`#24282B`)
- Never set body copy in a weight lighter than Book
- Never use the hero blue `#00A3E0` as a large background fill on a full page — it overwhelms
- Never substitute a different blue — the Pantone BW 299C match is exact and intentional
- Never place the color logo on a colored background without a white container
- Don't use lowercase-only labels — Brio labels are always uppercase
