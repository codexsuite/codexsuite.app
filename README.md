# codexsuite.app

The landing page for **Codex**, the open-source writing studio for non-fiction books and series. It is a single static page that says what Codex is and that it is open source and coming soon.

| Folder | What it is |
|---|---|
| [`site/`](site/) | The website. Plain HTML and CSS with no build step: `index.html`, `tokens.css`, `favicon.svg`, `og-image.png` and the screenshots in `shots/`. |
| [`design/`](design/) | Reference assets: logo and favicon, design tokens, full-resolution screenshots of every screen in light and dark, and the social card source. See [`design/README.md`](design/README.md). |

## Run it locally

Open `site/index.html` in a browser, or serve the folder:

```sh
npx serve site
```

## Deploy

The domain is on Cloudflare, so the simplest host is **Cloudflare Pages**:

1. In the Cloudflare dashboard, go to **Workers & Pages → Create → Pages → Connect to Git** and pick this repo.
2. Leave **Build command** empty and set **Build output directory** to `site`.
3. Under **Custom domains**, add `codexsuite.app`.

Any static host works the same way: publish the `site/` folder as the web root.

## Editing the page

- Colours, fonts and radii come from `site/tokens.css`, a copy of the Codex app's design tokens. Change the page's look there or in the `<style>` block in `index.html`, not with one-off hex values.
- Every screenshot exists in light and dark. The page shows the one that matches the visitor's theme, so add or replace both.
- Links to GitHub point at the [`codexsuite`](https://github.com/codexsuite) org. Point them at the app repo once it is public.
