# Brio Water — Agent Skills

Copy-paste recipes for common Brio-branded components.

---

## 1. Hero Banner

Full-width hero with headline, subtext, and CTA. Use on homepage and landing pages.

```html
<section class="brio-hero">
  <div class="brio-hero__content">
    <h1 class="brio-hero__headline">Feel Good About Your Water</h1>
    <p class="brio-hero__sub">
      Everything you need for better water, all in one place.
    </p>
    <div class="brio-hero__actions">
      <a href="/collections" class="brio-btn brio-btn--primary">Shop Now</a>
      <a href="/pages/about" class="brio-btn brio-btn--ghost">Learn More</a>
    </div>
  </div>
  <div class="brio-hero__media">
    <!-- Product or lifestyle image -->
  </div>
</section>
```

```css
.brio-hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  gap: var(--space-2xl);
  padding: var(--space-3xl) var(--content-padding);
  background: var(--surface-default);
  max-width: var(--max-width);
  margin: 0 auto;
}
.brio-hero__headline {
  font-family: var(--font-primary);
  font-size: var(--hero);
  font-weight: 700;
  color: var(--color-blue);
  line-height: 1.1;
}
.brio-hero__sub {
  font-size: var(--fs-body-l);
  color: var(--color-charcoal);
  margin-top: var(--space-l);
  max-width: 48ch;
}
.brio-hero__actions {
  display: flex;
  gap: var(--space-m);
  margin-top: var(--space-xl);
  flex-wrap: wrap;
}
@media (max-width: 768px) {
  .brio-hero { grid-template-columns: 1fr; }
}
```

---

## 2. Buttons

Primary (solid blue) and ghost (outlined). Labels always uppercase.

```html
<a class="brio-btn brio-btn--primary" href="#">Shop Now</a>
<a class="brio-btn brio-btn--ghost" href="#">Learn More</a>
<a class="brio-btn brio-btn--dark" href="#">View Details</a>
```

```css
.brio-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: var(--space-s);
  padding: 1.2rem 2.8rem;
  border-radius: var(--radius-l);
  font-family: var(--font-primary);
  font-size: var(--fs-label);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  text-decoration: none;
  cursor: pointer;
  border: 2px solid transparent;
  transition: opacity var(--dur-base) var(--ease-out),
              transform var(--dur-base) var(--ease-out);
}
.brio-btn:hover { opacity: 0.88; transform: translateY(-1px); }

.brio-btn--primary {
  background: var(--color-blue);
  color: var(--color-white);
}
.brio-btn--ghost {
  background: transparent;
  color: var(--color-blue);
  border-color: var(--color-blue);
}
.brio-btn--dark {
  background: var(--color-white);
  color: var(--color-navy);
}
```

---

## 3. Product Card

Standard e-commerce product card with badge, image, name, price, and quick-add.

```html
<div class="brio-product-card">
  <div class="brio-product-card__badge brio-product-card__badge--sale">50% OFF</div>
  <div class="brio-product-card__image">
    <img src="/product.png" alt="Brio 730 Series Dispenser" />
    <button class="brio-product-card__quick-add brio-btn brio-btn--primary">Quick Add</button>
  </div>
  <div class="brio-product-card__body">
    <p class="brio-product-card__series">Moderna Series</p>
    <h3 class="brio-product-card__name">Self-Cleaning Bottom Load Water Dispenser</h3>
    <div class="brio-product-card__pricing">
      <span class="brio-product-card__price--sale">$249.99</span>
      <span class="brio-product-card__price--original">$499.99</span>
    </div>
  </div>
</div>
```

```css
.brio-product-card {
  background: var(--color-white);
  border-radius: var(--radius-l);
  overflow: hidden;
  position: relative;
  box-shadow: var(--shadow-card);
  transition: box-shadow var(--dur-base) var(--ease-out),
              transform var(--dur-base) var(--ease-out);
}
.brio-product-card:hover {
  box-shadow: var(--shadow-hover);
  transform: translateY(-4px);
}
.brio-product-card__image {
  aspect-ratio: 1;
  background: var(--color-gray-light);
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
}
.brio-product-card__image img {
  width: 80%;
  height: 80%;
  object-fit: contain;
}
.brio-product-card__quick-add {
  position: absolute;
  bottom: var(--space-m);
  left: 50%;
  transform: translateX(-50%) translateY(8px);
  opacity: 0;
  transition: opacity var(--dur-base) var(--ease-out),
              transform var(--dur-base) var(--ease-out);
  white-space: nowrap;
}
.brio-product-card:hover .brio-product-card__quick-add {
  opacity: 1;
  transform: translateX(-50%) translateY(0);
}
.brio-product-card__badge {
  position: absolute;
  top: var(--space-m);
  left: var(--space-m);
  padding: 0.4rem 1rem;
  border-radius: var(--radius-s);
  font-size: var(--fs-micro);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  z-index: 1;
}
.brio-product-card__badge--sale  { background: var(--color-blue);  color: white; }
.brio-product-card__badge--new   { background: var(--color-navy);  color: white; }
.brio-product-card__body { padding: var(--space-l); }
.brio-product-card__series {
  font-size: var(--fs-label);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--color-blue);
  margin-bottom: var(--space-s);
}
.brio-product-card__name {
  font-size: var(--h4);
  font-weight: 500;
  color: var(--color-charcoal);
  line-height: 1.3;
}
.brio-product-card__price--sale {
  font-size: var(--fs-body-l);
  font-weight: 700;
  color: var(--color-blue);
}
.brio-product-card__price--original {
  font-size: var(--fs-body-s);
  color: var(--color-gray);
  text-decoration: line-through;
  margin-left: var(--space-s);
}
```

---

## 4. Dark Navy Feature Section

For callouts, feature highlights, USP blocks — use on dark navy background.

```html
<section class="brio-feature-dark">
  <div class="brio-feature-dark__inner">
    <span class="brio-label">Why Brio</span>
    <h2>Better Water is Better for All</h2>
    <p>Multi-stage filtration removes 99% of contaminants. NSF-certified. Built to last.</p>
    <a href="/pages/filtration" class="brio-btn brio-btn--dark">Explore Filtration</a>
  </div>
</section>
```

```css
.brio-feature-dark {
  background: var(--color-navy);
  color: var(--color-white);
  padding: var(--space-3xl) var(--content-padding);
  text-align: center;
}
.brio-feature-dark h2 {
  font-size: var(--h2);
  font-weight: 700;
  color: var(--color-white);
  margin: var(--space-m) 0;
}
.brio-feature-dark p {
  font-size: var(--fs-body-l);
  color: var(--color-blue-light);
  max-width: 56ch;
  margin: 0 auto var(--space-xl);
}
```

---

## 5. Stat / Trust Bar

Social proof strip — typically placed just below hero.

```html
<div class="brio-trust-bar">
  <div class="brio-trust-bar__item">
    <strong>99%</strong>
    <span>Contaminants Removed</span>
  </div>
  <div class="brio-trust-bar__item">
    <strong>NSF</strong>
    <span>Certified Components</span>
  </div>
  <div class="brio-trust-bar__item">
    <strong>1M+</strong>
    <span>Happy Customers</span>
  </div>
  <div class="brio-trust-bar__item">
    <strong>Free</strong>
    <span>Shipping on Orders $50+</span>
  </div>
</div>
```

```css
.brio-trust-bar {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  background: var(--color-gray-light);
  border-top: 1px solid var(--color-gray-light);
  border-bottom: 1px solid var(--color-gray-light);
}
.brio-trust-bar__item {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: var(--space-l) var(--space-m);
  border-right: 1px solid rgba(158, 161, 162, 0.3);
}
.brio-trust-bar__item:last-child { border-right: none; }
.brio-trust-bar__item strong {
  font-size: var(--h3);
  font-weight: 700;
  color: var(--color-blue);
}
.brio-trust-bar__item span {
  font-size: var(--fs-body-s);
  color: var(--color-gray);
  text-align: center;
  margin-top: var(--space-xs);
}
@media (max-width: 640px) {
  .brio-trust-bar { grid-template-columns: repeat(2, 1fr); }
}
```

---

## 6. Label / Badge

Uppercase label for series names, category tags, and product badges.

```html
<span class="brio-label">Moderna Series</span>
<span class="brio-label brio-label--navy">Bottleless</span>
<span class="brio-label brio-label--light">New Arrival</span>
```

```css
.brio-label {
  display: inline-block;
  font-family: var(--font-primary);
  font-size: var(--fs-label);
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--color-blue);
}
.brio-label--navy  { color: var(--color-navy); }
.brio-label--light { color: var(--color-gray); }
```
