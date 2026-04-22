# spilltop.com

Static site for [spilltop.com](https://spilltop.com) — landing page plus legal pages (Terms, Privacy, Community Guidelines) and Support. Designed for a simple GitHub + Cloudflare Pages deploy.

## Structure

```
/                 → landing page
/terms            → Terms of Service
/privacy          → Privacy Policy
/guidelines       → Community Guidelines
/support          → Support contact
/assets/styles.css  shared stylesheet
.nojekyll         disables Jekyll processing
```

Each page lives in its own folder with an `index.html`, so the URLs match `spilltop.com/terms` (no `.html` suffix).

## Deploying

1. Push to `main`.
2. In Cloudflare: **Workers & Pages → Create → Pages → Connect to Git**.
3. Select this repo.
4. Build command: leave empty.
5. Build output directory: `/`.
6. Add custom domains: `spilltop.com` and `www.spilltop.com`.
7. Wait for Cloudflare to create the DNS records and SSL certificate.

## Editing

Just edit the HTML files and commit. The dates at the top of each legal page live in `<span class="effective">` tags — update those when you make material changes.
