# Chikmagalur Filter Coffee — Vercel Ready

Premium static storefront + owner admin panel, prepared for deployment through **GitHub → Vercel**.

## Project structure

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
vercel.json
```

## Deploy with GitHub + Vercel

1. Create a GitHub repository.
2. Upload the **contents of this folder** directly into the repository root. Do not upload the ZIP itself and do not put the site inside another nested folder.
3. In Vercel, choose **Add New → Project** and import the GitHub repository.
4. Framework Preset: **Other** (or leave it as detected for a static site).
5. Build Command: **leave empty**.
6. Output Directory: **leave empty**.
7. Install Command: **leave empty**.
8. Click **Deploy**.

After deployment:

- Storefront: `https://YOUR-DOMAIN.vercel.app/`
- Admin: `https://YOUR-DOMAIN.vercel.app/admin`
- Admin direct URL: `https://YOUR-DOMAIN.vercel.app/admin.html`

`vercel.json` maps `/admin` to `admin.html` so the owner panel works cleanly on Vercel.

## Demo owner login

- Email: `owner@chikmagalurcoffee.in`
- Password: `coffeeadmin`

## Important limitation

The current admin panel is a **browser/localStorage prototype**. Product/content edits are stored only in the browser that made them. The login credentials are also present in frontend JavaScript, so this is not suitable as the security model for a real production store.

For a production coffee shop, the next version should use **Supabase Auth + Database + Storage**, with role-based access and Row Level Security. Razorpay should be integrated through a secure backend/Edge Function, with server-side payment verification and webhooks. Never put Razorpay secret keys or a Supabase service-role key in frontend code.
