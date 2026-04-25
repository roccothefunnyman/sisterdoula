# sisterdoula

Website for Rocco's sister, a doula.

## Live site

Deployed via GitHub Pages on every push to `main`:

- `https://roccothefunnyman.github.io/sisterdoula/`

A custom domain (purchased through Cloudflare) will be wired up later.

Three design previews are currently running side by side, with a picker at the root:

- `/` picker
- `/a/` editorial broadsheet
- `/b/` letterpress and botanical
- `/c/` quiet brutalism

## Stack

Plain static HTML + CSS. No build step, no JS framework. Open `index.html` in a browser to preview locally, no dev server needed.

If you'd rather run a local server (so relative paths behave like production):

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Structure

```
.
├── index.html       # picker page linking to the three previews
├── a/index.html     # preview A: editorial broadsheet
├── b/index.html     # preview B: letterpress and botanical
├── c/index.html     # preview C: quiet brutalism
├── CLAUDE.md        # working context for Claude Code
└── README.md
```

Each preview is self-contained (HTML + inline CSS + Google Fonts). Once a direction is chosen, the picker and unused previews come out and the chosen design moves to `/`.

## Deploying

GitHub Pages is configured to serve from the `main` branch root. Push to `main` and the site updates within ~1 minute.

To add a custom domain later:

1. Buy the domain (Cloudflare).
2. Add a `CNAME` file at the repo root containing the domain (e.g. `example.com`).
3. In Cloudflare DNS, add `A` records for GitHub Pages' IPs (or a `CNAME` for `www`). See [GitHub's docs](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site).
4. Enable "Enforce HTTPS" in the repo's Pages settings once DNS propagates.

## Status

Early scaffolding. Most copy is placeholder until we have:

- Sister's name / business name
- Service area (city/region)
- Service list
- Bio + photos
