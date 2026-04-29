# Brio Water — Product UI

Reusable patterns for Brio-branded e-commerce pages, landing pages, and product surfaces.

---

## Surface Model

| Role | Color | Use |
|---|---|---|
| **Default** | `#FFFFFF` white | Cards, content areas, default page bg |
| **Tint** | `#F0F8FD` | Alternating sections, light feature blocks |
| **Dark** | `#004D7A` navy | Feature callouts, promotional strips |
| **Footer** | `#24282B` charcoal | Site footer |

Never use `#00A3E0` (primary blue) as a large full-section background. It's too intense at scale — use it for text, CTAs, and accents only.

---

## Page Anatomy

### Homepage
```
┌─────────────────────────────────────┐
│  NAV (white, sticky)                │
├─────────────────────────────────────┤
│  HERO (white bg, blue headline)     │
├─────────────────────────────────────┤
│  TRUST BAR (gray-light strip)       │
├─────────────────────────────────────┤
│  FEATURED PRODUCTS (white, 4-col)   │
├─────────────────────────────────────┤
│  DARK FEATURE (navy bg)             │
├─────────────────────────────────────┤
│  CATEGORY GRID (tint bg)            │
├─────────────────────────────────────┤
│  LIFESTYLE CAMPAIGN (full bleed)    │
├─────────────────────────────────────┤
│  TESTIMONIALS (white, carousel)     │
├─────────────────────────────────────┤
│  PARTNER BADGES (gray-light strip)  │
├─────────────────────────────────────┤
│  FOOTER (charcoal)                  │
└─────────────────────────────────────┘
```

### Product Listing Page (PLP)
- Sticky filter sidebar left (desktop)
- Product grid right: 4-col desktop → 3-col tablet → 2-col mobile
- Sort bar top-right
- Active filters shown as dismissible chips (blue bg, white text)
- Breadcrumb navigation below header

### Product Detail Page (PDP)
- 2-column layout: images left, info right
- Image gallery: main image + thumbnail row
- Product name: H2, charcoal
- Series label: uppercase blue above name
- Price: H3 weight; sale price blue, original struck through
- "Add to Cart" full-width primary button
- Tab strip below fold: Description / Specs / Reviews

---

## Navigation

- White background, sticky on scroll
- Logo left (color version on white)
- Mega-menu center: categories with product images + sub-links
- Right: search icon, account icon, cart icon with count badge
- Mobile: hamburger → slide-in drawer, category accordion

**Nav item style:**
```css
font-family: var(--font-primary);
font-size: var(--fs-label);
font-weight: 500;
text-transform: uppercase;
letter-spacing: 0.06em;
color: var(--color-charcoal);
```

Active/hover: color shifts to `--color-blue`, no underline.

---

## Product Card System

**Default card:**
- White bg, `--radius-l` corners
- Blue shadow on hover (`--shadow-hover`)
- `translateY(-4px)` lift on hover
- Quick-add button reveals on hover (opacity 0 → 1)

**Badge variants:**
- Sale: blue bg (`#00A3E0`), white text
- New: navy bg (`#004D7A`), white text
- Exclusive: charcoal bg (`#24282B`), white text

**Product series label:** uppercase, `--color-blue`, above the product name.

---

## Campaign / Lifestyle Sections

Six recurring lifestyle themes used in hero banners and full-bleed campaigns:
1. **Good Habits** — morning routines, healthy hydration
2. **Take Care of Your Team** — office/workplace solutions
3. **Built to Last** — durability and engineering
4. **Better for the Planet** — sustainability, reduced plastic
5. **Refresh Your Space** — home/interior aesthetics
6. **Pure Performance** — filtration technology, specs

Each theme uses the same layout: full-bleed image, overlaid headline in white, primary CTA. Dark overlay on image minimum 40% opacity for text legibility.

---

## Interaction Principles

**Product cards:** Lift + shadow on hover. Quick-add slides up from bottom of image.
**Buttons:** `opacity: 0.88` + `translateY(-1px)` on hover. 220ms ease-out.
**Image zoom:** Product images zoom 1.04× on hover (within clip bounds).
**Filter chips:** Active state: solid blue bg. Hover: blue border + blue text.
**Scroll animations:** Fade + translateY(16px → 0), 380ms, Intersection Observer, staggered 60ms.

**Never:**
- Autoplay video on product pages without mute
- Animate price or quantity values unexpectedly
- Use parallax on product detail pages — it distracts from conversion

---

## Responsive Breakpoints

| Name | Width | Product grid |
|---|---|---|
| Mobile | `< 640px` | 2 columns |
| Tablet | `640px–1024px` | 3 columns |
| Desktop | `> 1024px` | 4 columns |
| Wide | `> 1320px` | Constrained to `--max-width` |

Trust bar collapses: 4-col → 2-col on mobile.
Mega-menu collapses: dropdown → accordion drawer on mobile.

---

## Don'ts

- Don't use `#00A3E0` as a full-section background — it reads as overload
- Don't mix more than 2 highlight hues in one composition
- Don't use card shadows with black — always blue-tinted (`rgba(0, 163, 224, …)`)
- Don't set product names in Light weight — minimum Book for legibility
- Don't place the logo on any colored background without proper clearance
