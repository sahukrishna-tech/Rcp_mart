# RCP E-Mart — Prototype

A lightweight, static click-through prototype covering all four roles: Buyer, Seller, Delivery Partner, and Admin. Plain HTML/CSS/JS — **no build step, no framework, no backend, no service worker** — so it loads instantly and reliably on GitHub Pages with nothing to go stale or lag.

## Run locally in VS Code
1. Open this folder in VS Code.
2. Install the **Live Server** extension (if you don't have it).
3. Right-click `index.html` → **Open with Live Server**.
   (Or just double-click `index.html` to open it directly in a browser — it works with no server at all.)

## Deploy to GitHub Pages
1. Create a new GitHub repo (e.g. `rcp-e-mart`).
2. Push everything in this folder to the repo root:
   ```
   git init
   git add .
   git commit -m "RCP E-Mart prototype"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. In the repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → Save.
4. Your live prototype link:
   `https://<your-username>.github.io/<repo-name>/`
   (usually live within a minute or two of the first push)

This is a single small HTML/CSS/JS bundle with no external dependencies except Google-hosted system fonts, so the GitHub Pages link should open instantly on any device — good for pulling up live on a projector or phone in front of officials.

## Get an installable `.apk` from the hosted link (optional)
1. Go to [pwabuilder.com](https://www.pwabuilder.com).
2. Paste in your GitHub Pages URL from above.
3. **Package for Stores → Android** → download the `.apk`.
4. Install it on an Android phone (allow "install from unknown sources" if prompted).

## Files
- `index.html` — page shell
- `style.css` — all styling (cream/red theme, cards, bottom nav, tabs, timeline)
- `app.js` — every screen, sample data, and click logic
- `manifest.json` — lets a phone add it to the home screen with the RCP E-Mart icon
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` — app icons
- `.nojekyll` — tells GitHub Pages to serve the files as-is

## Screens included (matches the 15-screen reference)
1. Welcome / role picker (Buyer, Seller, Delivery Partner, Admin) with English/Telugu toggle
2. Buyer Home — banners, categories, nearby vendors
3. Product Search & Compare
4. Vendor Profile
5. Cart & Checkout
6. Seller Dashboard
7. Add Product
8. Seller Orders (tabbed: New / Accepted / Preparing)
9. Delivery Partner — available orders
10. Delivery Flow — live tracking timeline
11. Admin — Vendor Approvals (tabbed: Pending / Approved / Rejected)
12. Promotion Request (seller banner submission)
13. My Rewards / Credits (buyer)
14. My Orders & Tracking (tabbed: All / Processing / Delivered)
15. Profile & Settings

## Not yet real
No backend, no persistence (state resets on refresh), no real photos (icons/emoji stand in), no payments/maps. This is a click-through prototype to demonstrate the concept and flow, not a production app.
