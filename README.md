# COFM Calculator

**Correlation of Forces and Means (COFM)** — a single-page, client-side calculator for force-ratio analysis. Drag-and-drop unit palette with MIL-STD-2525 symbology (via [milsymbol](https://github.com/spatialillusions/milsymbol)), posture modifiers, and exportable results.

> **Classification:** UNCLASSIFIED. All calculations run locally in the browser; no data leaves the client.

## Stack

- Pure static HTML / CSS / JavaScript — no build step.
- `milsymbol` loaded from jsDelivr CDN.
- Deployed on Vercel as a static site.

## Local preview

Open `index.html` directly in a browser, or serve it:

```bash
npx serve . -l 3000
# or
python3 -m http.server 3000
```

Then visit <http://localhost:3000>.

## Deploy on Vercel

Vercel auto-detects `vercel.json` and serves `index.html` as the root. Two options:

1. **Git integration (recommended).** Import the GitHub repo at <https://vercel.com/new>, accept defaults, deploy.
2. **CLI.**
   ```bash
   npm i -g vercel
   vercel            # preview deploy
   vercel --prod     # production deploy
   ```

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The application (self-contained). |
| `vercel.json` | Vercel static-hosting config + security headers. |
| `package.json` | Metadata + local `npm start` helper. |
| `.gitignore` | Standard ignores. |
