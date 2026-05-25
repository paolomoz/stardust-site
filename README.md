# stardust-site

Marketing site for [Stardust](https://github.com/adobe/skills/tree/main/plugins/stardust) — the design-phase toolkit. Built on [impeccable](https://impeccable.style/).

Live at **https://stardust.style/**.

## Pages

- `/` — home
- `/docs/` — install + getting-started (combined)
- `/docs/commands/` — command reference

## Local preview

The HTML uses absolute paths (`href="/docs/"`), so serve from this directory at the root:

```sh
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Deploy

`.github/workflows/pages.yml` rsyncs the site into a Pages artifact and uploads it. The `CNAME` file pins the custom domain (`stardust.style`). To enable: **Settings → Pages → Source: GitHub Actions**, then **Custom domain: stardust.style**.
