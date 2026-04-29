# Third Time Together — Squarespace Setup Guide

Requires **Business plan** (for Custom CSS + Code Blocks).

---

## Step 1 — Custom CSS
Design → Custom CSS → paste the entire contents of `custom.css`.

This sets your brand colors, Goldplay fonts, button styles, nav styling, and menu tab styles.

> **Font note:** The CSS loads Goldplay directly from your GitHub repo (`sladin/TTT`).  
> Make sure the repo is **public** or the fonts won't load.

---

## Step 2 — Announcement Bar
Settings → Advanced → Code Injection → **Header** → paste `announcement-bar.html`.

This adds the hours/location strip above the nav on every page.

---

## Step 3 — Navigation
Pages → Not Linked (or main nav) → add these pages:
- **Menu** (links to your menu page)
- **Gift Cards** (link to Square gift card URL)
- **Our Story** (links to the #our-story anchor on homepage)
- **Newsletter** (links to the #newsletter anchor on homepage)
- **Order Now** (links to your Square ordering URL) — mark as a Button style in nav settings

In Design → Site Styles, set nav background to `#EDEAD9` (cream).

---

## Step 4 — Homepage Sections

Build these sections top to bottom using the **+** button in the editor:

### Section 1: Hero (Banner)
- Block type: **Banner** or **Cover Page**
- Background: upload `images/interior.jpg`
- Set overlay color to `rgba(15,14,10,0.65)` in section background settings
- Add a **Text block** → type "Third Time Together" → set to Heading 1
- Add a **Code block** directly below → paste `hero-wave.html`
- Add a **Text block** → "Kendall Square · Cambridge, MA" → set to small/subtitle
- Add a **Text block** → the tagline paragraph
- Add **Button blocks** → Order Pickup, Order Delivery, View Menu

### Section 2: Intro Quote
- Block type: **Text** section, cream background
- Add a small label text: "All Day · Every Day"
- Add a large italic quote text block

### Section 3: Brand Stripe
- Block type: **Code**
- Paste `stripe-divider.html`

### Section 4: Photo Grid
- Block type: **Gallery** → set layout to Grid, 3 columns
- Upload: interior.jpg, sandwich.jpg, coffee.jpg, pita.jpg, icecream.jpg

### Section 5: Offer Strip
- Block type: **Text** section
- Type: `Breakfast · Lunch · Dinner · Ice Cream · Coffee & Tea · Stuffed Pitas`
- Set font to large italic

### Section 6: Brand Stripe
- Repeat Code block with `stripe-divider.html`

### Section 7: Order CTA
- Block type: **2-column** section
- Left: Text block with heading "Ready to eat?" + paragraph + button linking to menu
- Right: Two button blocks (Order Pickup, Order Delivery) with custom styling

### Section 8: Hours & Location
- Block type: **3-column** section, cream background
- Column 1: Location text
- Column 2: Hours text
- Column 3: Instagram link

### Section 9: Our Story
- Block type: **2-column** section
- Left: Text block with heading + paragraphs
- Right: Image block → upload `interior.jpg`

### Section 10: Newsletter
- Block type: **Newsletter** (Squarespace built-in) → black background
- Connect to Mailchimp or use Squarespace Email Campaigns
- Or use a **Form** block with an email field

### Section 11: Instagram
- Block type: **Instagram** (built-in block)
- Connect your @thirdtimetogether account
- Set to grid layout, 4 columns

---

## Step 5 — Menu Page

- Create a new **Page** called "Menu"
- Set the page background to `#3B4BC8` (blue) in section settings
- Add one **Code block** → paste the entire contents of `menu-tabs.html`
- That single block contains all four tabs with full menu content

---

## Step 6 — Footer
Design → Footer → add three columns:
- Left: Brand name + @thirdtimetogether Instagram link
- Center: Address
- Right: Hours

---

## Updating the Menu Later

To update menu prices or items, go to your Menu page → click the Code block → find the item in the HTML table and edit the text directly. Each item follows this pattern:

```html
<tr>
  <td>Item Name</td>
  <td align="right" style="color:#D97BAB;">$0.00</td>
</tr>
```

To add a new ice cream flavor, copy any `<div class="...flavor-card...">` block and paste it inside the flavors grid.
