# outly.app

Static site for [outly.app](https://outly.app) — landing page plus legal pages (Terms, Privacy, Community Guidelines). Served from GitHub Pages.

## Structure

```
/                 → landing page
/terms            → Terms of Service
/privacy          → Privacy Policy
/guidelines       → Community Guidelines
/assets/styles.css  shared stylesheet
CNAME             custom domain (outly.app)
.nojekyll         disables Jekyll processing
```

Each legal page lives in its own folder with an `index.html`, so the URLs match `outly.app/terms` (no `.html` suffix).

## Deploying

1. Push to `main`.
2. In the repo: **Settings → Pages** → source **Deploy from a branch** → branch **main** → folder **/ (root)** → Save.
3. Wait ~30 seconds. GitHub will show the live URL at the top of the Pages panel.
4. The `CNAME` file points GitHub Pages at `outly.app`. Create these DNS records at your registrar:

   | Type  | Host    | Value                    |
   |-------|---------|--------------------------|
   | A     | @       | 185.199.108.153          |
   | A     | @       | 185.199.109.153          |
   | A     | @       | 185.199.110.153          |
   | A     | @       | 185.199.111.153          |
   | CNAME | www     | sammygames123.github.io. |

5. Back on the Pages panel, enable **Enforce HTTPS** once the certificate finishes provisioning (can take 15–30 minutes after DNS resolves).

## Editing

Just edit the HTML files and commit. The dates at the top of each legal page live in `<span class="effective">` tags — update those when you make material changes.
