# caroldavidsen.com

A small static site for essays. No build step, no framework — plain HTML and one shared stylesheet. New essays follow the same pattern as `essays/cost-of-search.html`: copy that file, replace the content, add a matching `<li>` entry to `index.html`.

## Files

- `index.html` — home page, lists all essays
- `essays/cost-of-search.html` — "The Cost of Search" essay
- `styles.css` — shared styles for every page

## Deploying

This repo is meant to be connected directly to Cloudflare Pages (Workers & Pages → Create → Pages → Connect to Git). No build command is needed — set the framework preset to "None," leave the build command blank, and set the output directory to `/`.

See the deployment walkthrough for the full GitHub + Cloudflare Pages setup.
