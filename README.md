# NutriDac — Waitlist Landing Page

A mobile-first, single-file static site. No build step. Deploys to **Render** (free Static Site tier).

## Files
`index.html` · `logo.jpg` · `header-image.webp` · `favicon.svg` · `render.yaml`

## Deploy to Render
Render reads `render.yaml` automatically (Blueprint), so:

1. Push this folder to a GitHub repo.
2. [Render Dashboard](https://dashboard.render.com) → **New → Blueprint** → pick the repo → **Apply**.
   *(Manual alternative: New → Static Site → Build Command: blank · Publish Directory: `./`)*
3. Live in ~1 min at `https://nutridac.onrender.com` with free HTTPS.
4. Custom domain: service → **Settings → Custom Domains** → add `nutridac.com` and set the DNS record Render shows.

Every `git push` auto-redeploys.

## ⚠️ Make the form capture real signups (2 min)
The waitlist form runs in **DEMO mode** until you add a free Web3Forms key — right now it shows the success state but stores nothing.

1. Go to **https://web3forms.com** → enter your email → copy the **Access Key** (no password/signup).
2. In `index.html`, find `const WEB3FORMS_KEY = "REPLACE_WITH_YOUR_WEB3FORMS_ACCESS_KEY";` and paste your key.
3. Commit & push → Render auto-redeploys. Signups now email you (and can forward to a Google Sheet from the Web3Forms dashboard).
