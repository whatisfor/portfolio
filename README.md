# whatisfor — portfolio

A dependency-free static portfolio site: one HTML page, one stylesheet, one
small script. No build step.

## Structure

```
public/
  index.html   # the whole site
  styles.css   # design tokens + layout
  script.js    # theme toggle + scroll reveal
  404.html     # served for unknown routes
wrangler.jsonc # Cloudflare Workers static-assets config
```

## Run locally

Any static server works:

```sh
npx --yes serve public
```

## Deploy

```sh
npx wrangler deploy
```

Wrangler publishes `public/` as static assets on a Worker and prints the live
URL.

## Make it yours

Everything editable lives in `public/index.html`:

- **Name & tagline** — the `.hero__title` and `.hero__lead` blocks
- **About** — the `#about` section
- **Projects** — three `.card` articles in `#projects`; update the title,
  description, tags, and the `<a href>` source links
- **Skills** — the three `.skill` blocks in `#skills`
- **Contact** — the `mailto:` address and the `#contact` social links

Colours are CSS custom properties at the top of `styles.css`, in both `:root`
(dark) and `html[data-theme="light"]`.
