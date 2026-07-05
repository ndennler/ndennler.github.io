# ndennler.github.io

Source for [Nathan Dennler](https://ndennler.github.io)'s personal academic website, built with Jekyll on the [Bay theme](https://github.com/eliottvincent/bay) and hosted on GitHub Pages.

The site includes:
- **Home** ([index.md](index.md)) — bio, news, and selected publications
- **Research** ([research.md](research.md)) — full publication list
- **CV** ([cv.md](cv.md))
- **Outreach** ([outreach.md](outreach.md))
- **Miscellany** ([miscellany.md](miscellany.md))

Site-wide settings (nav pages, footer/contact links, description, etc.) live in [_config.yml](_config.yml).

### Development

Install dependencies:
```sh
bundle install
```

Run a local dev server with hot-reload:
```sh
bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

> **Note:** When viewing posts locally, the auto-generated post URL (e.g. `http://0.0.7.232/09/17/some-post`) doesn't resolve correctly. Use `http://localhost:4000//<year>/<month>/<day>/<post-title>` instead (note the double slash). This only affects local dev — it works fine once deployed.

### Deployment

The site is published via GitHub Pages from this repo.
