#UK Government Linked Data Working Group Site

## The 9 steps process to contribute

### Markdown

Articles, guides, recommendations, everything here is writen in [Markdown](http://en.wikipedia.org/wiki/Markdown). If you never tried Markdown you'll get used to it soon as it's really easy. You can write markdown in any text editor, some are better because you can preview your file directly, but you can also just try a [markdown preview site](http://markdownlivepreview.com). Another solution you may enjoy would be [prose.io](http://prose.io) that allows you to edit your github's markdown files easily. 

### Step by step

You need to have [git](http://git-scm.com) and [gem](https://rubygems.org/pages/download) installed.

1. Clone the github repo

    `$ git clone https://github.com/UKGovLD/ukgovldwg.git`

    `$ cd ukgovldwg/`

2. Run the server

    `$ gem install jekyll`

    `$ jekyll serve`

    Then go to [http://localhost:4000/](http://localhost:4000/)

3. Create your file

    In `guides/`, `recommendations/` or `case-studies/` create your new file `your-file-name.md`

4. Use the template

    In each repository,there is a `*-template.md` file, copy-paste the content in your new file.

5. Write your content

    And don't forget to save your markdown file when it's done.

6. Add pictures

    You can add pictures in markdown, from an url:
    
    `![text-image](url-of-the-picture)`

    or by putting the picture in `assets/images`:

    `![text-image](../assets/images/name-of-the-picture.jpg)`

7. Add it to the site

    In the `_data/` repository, there are some `.yml` files, if you've writen a guide: open `guides.yml`. Now you can add your article in the corresponding section by adding `- your-file-name`

8. Check everything

    Go to [localhost](http://localhost:4000), check if everything is as you wanted.

9. Push it to GitHub

    `$ git add --all`
    
    `$ git commit -m "what have you done?"`

    `$ git push`
    
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
