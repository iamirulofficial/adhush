# AdHush Hosted Legal Pages

Static HTML pages required by Apple for App Store submission:
- `index.html` — Marketing landing page
- `privacy.html` — Privacy Policy (REQUIRED by Apple)
- `terms.html` — Terms of Use
- `support.html` — Support & FAQ (REQUIRED by Apple as Support URL)
- `style.css` — Shared styling

## Deploy to GitHub Pages (fastest, free)

1. Create a new GitHub repo, e.g. `adhush-app`
2. Copy these four HTML files + `style.css` to the repo root (or into a `/docs` folder)
3. Settings → Pages → Source: `main` branch → `/` (or `/docs`) → Save
4. Wait ~30 seconds, your site is live at `https://<username>.github.io/adhush-app/`
5. Use these URLs in App Store Connect:
   - **Privacy Policy URL**: `https://<username>.github.io/adhush-app/privacy.html`
   - **Support URL**: `https://<username>.github.io/adhush-app/support.html`
   - **Marketing URL** (optional): `https://<username>.github.io/adhush-app/`

## Deploy to Cloudflare Pages (free, custom domain easy)

1. Sign in to Cloudflare → Workers & Pages → Create application → Pages → Connect to Git
2. Pick the repo, set Build command to (none), output dir to `/`
3. Deploy. URL pattern: `adhush-app.pages.dev/privacy.html`
4. Optional: bring your own domain (e.g. `adhush.app`) in Custom domains tab

## Deploy to a custom domain (e.g. adhush.app)

1. Buy the domain (~$15/year on Cloudflare Registrar or Namecheap)
2. Use either GitHub Pages (point a CNAME record at `<username>.github.io`) or Cloudflare Pages (point an A/AAAA record at Cloudflare's edge)
3. Final URLs:
   - `https://adhush.app/privacy.html`
   - `https://adhush.app/support.html`

## After deploying

1. Open App Store Connect → AdHush → App Information
2. Paste your Privacy Policy URL
3. Open App Information → General Information → Support URL → paste support URL
4. (Optional) Marketing URL → paste index.html URL

The in-app `LegalSheet` also opens these URLs via Safari deep links, so the hosted version and the in-app text stay in sync.
