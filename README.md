# caroldavidsen.com

A small static site for essays. No build step, no framework — plain HTML and one shared stylesheet. New essays follow the same pattern as `essays/cost-of-search.html`: copy that file, replace the content, add a matching `<li>` entry to `index.html`.

## Files

- `index.html` — home page: About/bio section with LinkedIn and email links, the essay list, a Talks & Research section (kept here, not mixed with press, until it's big enough to warrant its own page), and a one-line teaser linking to `press.html`
- `press.html` — full media-coverage page (press citations only — talks and research live on the home page instead)
- `essays/cost-of-search.html` — "The Cost of Search" essay
- `styles.css` — shared styles for every page

## Adding a new press citation

Add a new `<li>` to the `<ul class="citation-list">` in `press.html`, following the existing pattern (`citation-source`, `citation-title` with a link, `citation-note`).

## Adding a new talk or research citation

Same pattern, but add it to the `<ul class="citation-list">` under "Talks & research" in `index.html` instead, since that section is being kept on the home page for now. If that list grows enough to warrant its own page, move it out the same way `press.html` was split off and update this README.

## Adding a photo later

`index.html`'s About section currently has no image. To add one, drop the image file at the repo root (or an `/images/` folder) and add an `<img>` tag above the `.bio` paragraph; `styles.css` doesn't yet have a rule for it, so a small addition there (sizing, border-radius, float/alignment) will be needed too.

## Deploying

This repo is meant to be connected directly to Cloudflare Pages (Workers & Pages → Create → Pages → Connect to Git). No build command is needed — set the framework preset to "None," leave the build command blank, and set the output directory to `/`.

See the deployment walkthrough for the full GitHub + Cloudflare Pages setup.
