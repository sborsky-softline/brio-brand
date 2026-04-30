# Brio Water — E-commerce UI Kit

A high-fidelity recreation of the Brio Water e-commerce surface (homepage,
PLP, PDP) using the brand tokens. Components are factored as small JSX
modules and composed in `index.html`.

## Components

- `Nav.jsx` — sticky white header with logo, nav, search/account/cart.
- `Hero.jsx` — 2-up hero with H1 in blue, body L subtext, dual CTAs.
- `TrustBar.jsx` — gray-light strip with 4 stat items.
- `ProductCard.jsx` — image + badge + series + name + price; hover lift.
- `ProductGrid.jsx` — 4-up grid for featured products.
- `DarkFeature.jsx` — navy bg callout with white CTA.
- `CategoryGrid.jsx` — 3-up category cards on tint background.
- `Footer.jsx` — charcoal footer with link columns + brand line.
- `Button.jsx` — primary / ghost / dark variants.

## Pages

`index.html` is the homepage. It demonstrates:
1. Nav with cart counter
2. Hero with primary CTA
3. Trust bar
4. Featured product grid (with hover quick-add)
5. Dark-navy feature callout
6. Category grid on tint section
7. Charcoal footer

## Notes

These are visual recreations that match the Brio brand spec
(`tokens.css`, `BRAND.md`, `PRODUCT_UI.md`). Real product photography is
substituted with simple SVG placeholders. Nav links and cart are not wired
to a real backend.
