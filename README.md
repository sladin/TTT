# Third Time Together — Website

Static site for **Third Time Together**, 399 Binney St, Kendall Square, Cambridge MA.

---

## Quick Setup

### 1. Photos

Add your photos to the `images/` folder with these exact filenames:

| Filename | Photo |
|----------|-------|
| `hero.jpg` | Night exterior — storefront with illuminated sign |
| `interior.jpg` | Sunny interior — ice cream counter, plants, bookshelves |
| `sandwich.jpg` | Breakfast sandwich on pink plate |
| `pita.jpg` | Stuffed pita with braised meat and citrus salsa on pink tray |
| `coffee.jpg` | Latte art in the blue glass |
| `icecream.jpg` | Two scoops in the pink bowl |
| `patio.jpg` | Outdoor patio with hyacinths and pansies |

JPEGs at least 1200×800px work best. The site handles scaling automatically.

### 2. Fonts

Fonts are already in `fonts/` — all six Goldplay OTF weights used by the site:
- Goldplay-Regular.otf
- Goldplay-RegularIt.otf
- Goldplay-Bold.otf
- Goldplay-BoldIt.otf
- Goldplay-Black.otf
- Goldplay-BlackIt.otf

### 3. Ordering Links

Find every `href="#"` in `index.html` and replace `#` with your Square URL:
- **Order Pickup** (2 places: hero + CTA section)
- **Order Delivery** (2 places: hero + CTA section)

---

## Updating Content

### Menu Items

Each item in `menu.html` looks like this:
```html
<li class="menu-item">
  <div>
    <span class="menu-item-name">Item Name</span>
    <span class="menu-item-desc">Description here</span>
  </div>
  <span class="menu-item-price">$0.00</span>
</li>
```

Without a description:
```html
<li class="menu-item">
  <span class="menu-item-name">Item Name</span>
  <span class="menu-item-price">$0.00</span>
</li>
```

### Ice Cream Flavors

Find the `id="tab-icecream"` section. Each flavor:
```html
<div class="flavor-card">
  <p class="flavor-name">Flavor Name</p>
  <p class="flavor-desc">Description of the flavor</p>
  <!-- Optional: -->
  <span class="flavor-tag">vegan</span>
</div>
```

---

## Deploying

### GitHub Pages

1. Create a new repo (e.g. `thirdtimetogether-site`)
2. Push this folder to `main`
3. Go to **Settings → Pages → Deploy from branch → main → / (root)**
4. Live at `https://yourusername.github.io/thirdtimetogether-site/`

For a custom domain: add a `CNAME` file with just `thirdtimetogether.com` and point DNS to GitHub Pages.

### Netlify (Fastest)

Drag and drop this entire folder onto **app.netlify.com/drop** — live in seconds. Connect to GitHub for auto-deploy on push.

---

## Notes

- **Instagram section**: The four placeholder tiles in `index.html` can be swapped for a real Instagram embed. The comment in the HTML marks the spot.
- **No build step**: Pure HTML/CSS/JS — open `index.html` in any browser to preview locally.
