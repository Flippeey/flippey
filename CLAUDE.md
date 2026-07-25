# flippey — Flippey's Software Hub

Public marketing site for Flipp's Favorites, served at **https://flippflix.com** (see `CNAME`).
Plain static HTML + CSS — no framework, no build step, no package manager.

**This site is public and every push ships it.** GitHub Pages serves straight from the branch,
so there is no build gate and no staging: a commit to the default branch is a production deploy
of a public page. Treat it accordingly — proofread copy, and check a change renders before pushing
rather than after.

Related repos: the extension itself is `Flippeey/flipps-favorites`; the sync backend is
`Flippeey/flippflix-sync`, which serves `api.flippflix.com` — same domain, different repo, so
don't look for API code here.

## Layout

```
index.html          # the entire site — single page
styles/
  tokens.css        # design tokens; loaded first, the other two build on it
  site.css          # main styles
  extras.css        # supplemental styles
assets/
  promo-gifs/       # feature GIFs used on the page
  shots/            # light/dark screenshot pairs
  *.png             # icons and logos; ref_* and shot-ref* are source references, not shipped
promo/              # promo working files
```

## Verification

No test suite and nothing to build. Open `index.html` in a browser, or serve the directory:

    python3 -m http.server 8000

Check both light and dark — the screenshots come in `-light` / `-dark` pairs and the page
switches between them.

## Gotchas

- **Lucide is pinned with an SRI hash.** `index.html` loads
  `unpkg.com/lucide@<version>` with an `integrity="sha384-..."` attribute. Bumping the version
  without regenerating that hash makes the browser silently refuse the script — every icon
  vanishes and there is no visible error on the page. Change both or neither.
- **Promo assets are coupled to the extension's released version.** The GIFs and screenshots are
  re-captured per extension release (see the `promo-realign` commits). A UI change shipped in the
  extension makes the assets here stale, and nothing detects that automatically.
- **`assets/ref_*` and `assets/shot-ref*` are reference source images**, not files the page loads.
  Don't wire them into `index.html`.

## Rules

- Style order matters: `tokens.css` → `site.css` → `extras.css`. New tokens go in `tokens.css`,
  not inlined.
- No analytics, no trackers, no third-party embeds beyond the pinned icon library. The extension's
  selling point is privacy; the site should not undercut it.
- Keep it dependency-free. If something seems to need a build step, discuss before introducing one.
