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

## Hosting

Live at **https://jv5rconsulting.com**, served by GitHub Pages from `main` (repo
`JV5RConsulting/jv5r-site`, Settings → Pages). Pushing to `main` deploys in about a minute. The `CNAME`
file holds the custom domain; do not delete it.

DNS is at Cloudflare (the registrar), every record **DNS only** (grey cloud), never Proxied, or GitHub
cannot renew the HTTPS certificate:

| Type | Name | Content |
|---|---|---|
| A | `@` | `185.199.108.153`, `.109.153`, `.110.153`, `.111.153` |
| CNAME | `www` | `jv5rconsulting.github.io` |
| TXT | `@` | `v=spf1 -all` (the domain sends no email) |
| TXT | `_dmarc` | `v=DMARC1; p=reject; ...` (reject spoofed mail) |

If the domain ever gets real email (Google Workspace, Cloudflare Email Routing), replace the two TXT
records with the provider's.

The Meta app (Content Curator) points at `https://jv5rconsulting.com/privacy.html` and
`https://jv5rconsulting.com/data-deletion.html`: keep those paths.

## Editing the copy

Keep it true: Marketing Video Studio quotes this page in videos and Content Curator cites those facts in
captions. Add a claim only when it is a fact about the business.
