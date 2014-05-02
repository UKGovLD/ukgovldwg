## Site Organisation

Jekyll is about to release v2.0 which incorporates a major new feature, _collections_.

We should adopt this feature as soon as GitHub Pages supports it, but in the interim, we will use the _data feature (partially) to emulate it, with a little manual maintenance.

This is a trade-off, between automation and control, and we've erred towards control (in the hope that collections will return a little of the automation!)
Consequently, making a new page live requires us manually to add the page to the collections in _data/ but has the advantages that we can control the sort order in which pages appear in the navigation, and that article permalinks are manually createed.

Our site structure is in part modelled on that of the Jekyll project's own site https://github.com/jekyll/jekyll/tree/master/site in the hope that this represents a forwards-compatible scheme.

## Assets

Also coming in Jekyll 2.0 is support for SASS.
Until then, the compiled stylesheet is in the repo, and can be regenerated if needed with

sass _sass/main.scss assets/css/main.css

Tip: you might find it convenient to alias something to

sass _sass/main.scss assets/css/main.css; jekyll build

## Stylesheets

data.gov.uk is built on Bootstrap 3 so we are too.
