# sisterdoula

Website for Rocco's sister, a doula.

## Live site

Deployed via GitHub Pages on every push to `main`:

- `https://<username>.github.io/sisterdoula/`

A custom domain (purchased through Cloudflare) will be wired up later.

## Stack

Plain static HTML + CSS. No build step, no JS framework. Open `index.html` in a browser to preview locally — no dev server needed.

If you'd rather run a local server (so relative paths behave like production):

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Structure

```
.
├── index.html       # landing page
├── styles.css       # all styles
├── CLAUDE.md        # working context for Claude Code
└── README.md
```

## Deploying

GitHub Pages is configured to serve from the `main` branch root. Push to `main` and the site updates within ~1 minute.

To add a custom domain later:

1. Buy the domain (Cloudflare).
2. Add a `CNAME` file at the repo root containing the domain (e.g. `example.com`).
3. In Cloudflare DNS, add `A` records for GitHub Pages' IPs (or a `CNAME` for `www`) — see [GitHub's docs](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site).
4. Enable "Enforce HTTPS" in the repo's Pages settings once DNS propagates.

## Status

Early scaffolding. Most copy is placeholder until we have:

- Sister's name / business name
- Service area (city/region)
- Service list
- Bio + photos
