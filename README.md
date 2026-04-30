# stardust-site

Marketing site for [Stardust](https://github.com/adobe/skills/tree/main/plugins/stardust) — the design-phase toolkit. Built on [impeccable](https://impeccable.style/).

Live at **https://paolomoz.github.io/stardust-site/**.

## Pages

- `/` — home
- `/docs/` — docs hub (Install)
- `/docs/getting-started/` — installation walkthrough
- `/docs/commands/` — command reference

## Local preview

The HTML uses absolute paths (`href="/docs/"`), so serve from this directory at the root:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Deploy

`.github/workflows/pages.yml` rewrites absolute paths to `/stardust-site/...` at build time so they resolve under the project-page subpath, then uploads as a Pages artifact. To enable: **Settings → Pages → Source: GitHub Actions**.
