# Chikmagalur Filter Coffee — GitHub Pages Edition

Premium static storefront + owner admin panel, prepared for **GitHub Pages**.

## Files
- `index.html` — storefront
- `admin.html` — owner admin panel
- `admin/` — friendly `/admin/` URL that opens `admin.html`
- `assets/` — product/brand images
- `.nojekyll` — keeps GitHub Pages deployment simple

## Deploy on GitHub Pages
1. Create a GitHub repository.
2. Upload **the contents of this folder** directly to the repository root. Do not upload the ZIP itself and do not put the site inside another nested folder.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then Save.
6. Open the GitHub Pages URL shown by GitHub.

The repository should look like:

```text
index.html
admin.html
admin/
  index.html
assets/
  brass-coffee.png
  cafe-facade.png
  heritage-badge.png
  heritage-blend.png
  still-life.png
style.css
script.js
admin.css
admin.js
.nojekyll
```

## Admin URLs
Both of these work on GitHub Pages:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/admin.html
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/admin/
```

### Demo owner login
- Email: `owner@chikmagalurcoffee.in`
- Password: `coffeeadmin`

## Important limitation
This admin panel is a **browser/localStorage prototype**. Changes are saved only in the browser that made them; GitHub Pages cannot provide a secure shared database by itself.

For a real store, connect the panel to **Supabase Auth + Database + Storage**, then connect **Razorpay** through a secure server/Edge Function with payment verification and webhooks. Never put Razorpay secret keys or database service-role keys in frontend JavaScript.
