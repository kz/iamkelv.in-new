# iamkelv.in

[ ![Codeship Status for kz/iamkelv.in](https://app.codeship.com/projects/af0d93a0-3b5a-0135-76f0-46ceed86863a/status?branch=master)](https://app.codeship.com/projects/228750)

This is the repository for my site (built in Jekyll), [https://iamkelv.in/](https://iamkelv.in/).

## Features

This site is loosely based on [jekyll/minima](https://github.com/jekyll/minima), initially created using the `jekyll new` command. The minima theme has been removed and replaced with my own design from scratch, however Google Analytics, Disqus comments and basic scaffolding remain. The following features have been added:

- A `_projects` collection has been added to list my projects
- The permalink of blog posts has been changed to `/blog/:year/:month/:title.html`
- A few plugins for SEO, including `jekyll-feed`, `jekyll-last-modified-at` and `jekyll-sitemap`
- `htmlproofer` to test internal links
- In the `_sass` folder: `_base.scss` contains the contents of [normalize.css](https://necolas.github.io/normalize.css/); `_flex.scss` contains code from [philipwalton/solved-by-flexbox](https://github.com/philipwalton/solved-by-flexbox); `_layout.scss` contains the site's main theme

## Installation

To install this Jekyll site, assuming you have installed Jekyll's [requirements](https://jekyllrb.com/docs/installation/), simply clone it to a directory and run:

1. Run `bundle install`
2. Run `jekyll serve` for development or `jekyll build` for deployment

### Testing

For CI (with CodeShip), I use the following script to build my site and check that internal links are valid (reporting any errors during this process):

```sh
bundle exec jekyll build
bundle exec htmlproofer ./_site --disable-external
```

## License

The CSS and boilerplate for this site is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT). See [LICENSE.md](LICENSE.md) for more details.

All other content, including blog posts and textual content, are _not_ open source (i.e., the MIT License does _not_ cover this) and the copyright is held by the author.
