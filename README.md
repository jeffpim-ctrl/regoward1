# Re-Elect Frank Rego — Ward 1, East Providence

Campaign website for Frank Rego's 2026 re-election to the East Providence City Council, Ward 1.

**Election day: Wednesday, September 9, 2026 (non-partisan primary).**

## Structure

```
index.html          The site (single page)
404.html            Not-found page served by GitHub Pages
css/style.css       All styles (design tokens at the top)
assets/img/         Optimized photos, logo, favicon, social share image
assets/fonts/       Self-hosted Lato + Roboto Slab (latin subset, woff2)
```

No build step, no dependencies — plain HTML and CSS. Edit `index.html` for content, `css/style.css` for styling. Brand colors are defined once as CSS variables at the top of the stylesheet.

## Deploying to GitHub Pages

1. Push this folder to a GitHub repository (e.g. `rego-ward1`).
2. In the repo: **Settings → Pages → Source: Deploy from a branch**, select `main` and `/ (root)`.
3. The site publishes at `https://<username>.github.io/rego-ward1/`.

The canonical/Open Graph URLs in `index.html` point at the live site: `https://regoward1.com/`. If the domain ever changes, update those URLs — they are what Facebook uses to build the link-preview card.

Using a custom domain (e.g. `frankrego.com`): add the domain under **Settings → Pages → Custom domain**, point the domain's DNS at GitHub Pages, and update the URLs above to match.

## Previewing locally

Any static server works:

```
python3 -m http.server 8080
```

Then open http://localhost:8080.

## Notes

- The `og-image.jpg` (1200×630) is the photo shown when the site link is shared on Facebook or elsewhere. After changing it, refresh Facebook's cache at https://developers.facebook.com/tools/debug/
- Fonts are subset to latin characters to keep the page fast. If non-latin text is ever added, regenerate subsets from Google Fonts.
- The footer disclaimer ("Paid for by…") is required on campaign materials — keep it on every page.
