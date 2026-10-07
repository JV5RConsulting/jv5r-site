# jv5r-site

The JV5R Consulting website: a static landing page plus the privacy policy and data-deletion pages the
Meta app (Content Curator) needs. Plain HTML and CSS, no build step, hosted on GitHub Pages.

| File | Purpose |
|---|---|
| `index.html` | Landing page. Marketing Video Studio reads it for facts, so every claim on it must be true. |
| `privacy.html` | Privacy policy (Meta app setting: Privacy Policy URL) |
| `data-deletion.html` | Data deletion instructions (Meta app setting: User data deletion URL) |
| `assets/icon-1024.png` | Meta app icon (1024x1024) |
| `assets/og-image.jpg` | Link preview image (1200x630) |

## Preview locally

Open `index.html` in a browser.

## Publish on GitHub Pages

1. Create a **public** GitHub repo named `jv5r-site` and push this folder to `main`.
2. Repo **Settings → Pages**: Source **Deploy from a branch**, branch `main`, folder `/ (root)`, Save.
3. A minute later it is live at `https://<github-user>.github.io/jv5r-site/`.

## Custom domain (after buying it)

1. At the registrar, add DNS records:
   - `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www`: `<github-user>.github.io`
2. Repo **Settings → Pages → Custom domain**: enter the domain, Save (GitHub commits a `CNAME` file).
3. When the certificate is ready, tick **Enforce HTTPS**.
4. Update the Meta app's Privacy Policy and Data deletion URLs to the new domain.

## Editing the copy

Keep it true: Marketing Video Studio quotes this page in videos and Content Curator cites those facts in
captions. Add a claim only when it is a fact about the business.
