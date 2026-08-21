# Transformers from Scratch, Revisited

A rebuild of Brandon Rohrer's 2021 essay [*Transformers from Scratch*](https://brandonrohrer.com/transformers.html)
(released CC0), with factual corrections, a modern decoder-only architecture, a full positional-encoding
chapter (RoPE), and the residual-stream perspective. Green on black, as remembered.

## Hosting on GitHub Pages

1. Push this directory to a GitHub repository (as the repo root).
2. Repo **Settings → Pages → Source**: *Deploy from a branch*, branch `main`, folder `/ (root)`.
3. The essay appears at `https://<username>.github.io/<repo>/` within a minute or two.

No build step, no dependencies. Fonts load from Google Fonts; everything else is local.

## Structure

```
index.html            the core essay
assets/style.css      shared stylesheet (phosphor theme, residual-stream margin line)
doors/                future expansion pages ("amber doors", §22 of the essay)
doors/_template.html  starting point for a new door page
.nojekyll             tells Pages to serve files as-is
LICENSE               CC0 1.0
```

## Adding a door page

1. Copy `doors/_template.html` to `doors/<slug>.html` (e.g. `doors/kv-cache.html`) and write it.
2. In `index.html`, find the matching `.stub` card in §22:
   - wrap the card's `<h3>` text in `<a href="doors/<slug>.html">…</a>`
   - change its `<span class="tag">` from `door NN · planned page` to `door NN · open`
3. Commit and push; Pages redeploys automatically.

## Corrections

§23 of the essay is a corrections ledger. If you find an error, open an issue — accepted
corrections get a ledger row and a line in the git history, which is the point.

## License

CC0 1.0 Universal, matching the original essay's dedication. Use any of it for anything;
a mention of the lineage (Rohrer 2021 → this) is appreciated, never required.
