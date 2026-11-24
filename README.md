# seungyubhan.github.io

Source for my personal page, <https://seungyubhan.github.io>. Pushing to `main` builds the site and deploys it to the `gh-pages` branch.

## Adding a paper

Add a file under `_posts/` (copy an existing one) and its thumbnail under `images/`. `categories: research` puts it under Publications, `categories: preprint` under Preprints.

## CV

The CV is built from `cv/main.tex`; publications live in `cv/pub_with_sortkey.bib`. The deploy workflow compiles it and publishes it at `/pdfs/cv_hsy.pdf`, so the PDF is not committed. To preview locally, run `latexmk main.tex` inside `cv/` and open `cv/build/main.pdf`.

## Credits

Built on [Jekyll Now](https://github.com/barryclark/jekyll-now). The design is a modification of [Jon Barron's website](https://jonbarron.info/).
