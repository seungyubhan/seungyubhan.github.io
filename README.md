# seungyubhan.github.io

Source for my personal page, <https://seungyubhan.github.io>. Pushing to `main` builds the site and deploys it with GitHub Pages Actions (`.github/workflows/pages.yml`).

## Adding a paper

Add a file under `_posts/` (copy an existing one) and its thumbnail under `images/`. `categories: research` puts it under Publications, `categories: preprint` under Preprints.

## CV

The CV is built from `cv/main.tex`; publications live in `cv/pub_with_sortkey.bib`. The deploy workflow compiles it and publishes it at `/pdfs/cv_hsy.pdf`, so the PDF is not committed. To preview locally, run `latexmk main.tex` inside `cv/` and open `cv/build/main.pdf`.

## Rolling back the deploy method

The site used to be built by `jekyll-deploy-action` and served from the `gh-pages` branch. That branch still holds the last site built that way, and the old workflow is kept as `.github/workflows/legacy-gh-pages.yml` (manual trigger only). To go back:

1. Settings → Pages → Source: "Deploy from a branch", branch `gh-pages`, folder `/`. The old copy of the site is live again as soon as this is saved.
2. To refresh it with the current `main`, run "Legacy deploy to gh-pages branch (fallback)" from the Actions tab.
3. To make that permanent, restore `on: push` (branch `main`) in the legacy workflow and delete `pages.yml`.

## Credits

Built on [Jekyll Now](https://github.com/barryclark/jekyll-now). The design is a modification of [Jon Barron's website](https://jonbarron.info/).
