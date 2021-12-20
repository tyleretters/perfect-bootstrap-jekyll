# Perfect Bootstrap Jekyll

## Setup Instructions

1. Clone repository to your computer.
2. Using terminal, navigate to the `perfect-jekyll` directory with `cd`.
3. In the directory execute: `bundle exec jekyll serve --baseurl ''`.
4. Visit [http://127.0.0.1:4000](http://127.0.0.1:4000) in your browser.
5. To work with the CSS: `cd assets/stylesheets` and run `sass --watch style.sass:style.css`.

Note: I use [rvm](https://rvm.io/). This incarnation of Perfect Bootstrap Jekyll was made with `ruby 2.7.2p137 (2020-10-01 revision 5445e04352) [arm64-darwin21]`.

## Navigation

Configure main navigation with `_data/nav.yml`.

## Metadata

Because Jekyll requires restarting if you change the `_config.yml`, I've moved some the values that you'll typically be adjusting regularly to `_data/meta.yml`. You can add whatever arbitrary values you wish here.

## Favicons

Favicon/Apple/Android icon markup is in head.html. Generate your icons at [favicon.io](https://favicon.io) and just dump all the assets into the top level directory of the repo. The paths should all be accurate.

## Sitemap

Open up `robots.txt` and update the URL.

## "Production" Class

The `<body>` element has `class="production"` added to it when served from GitHub Pages. Feel free to take it out if you don't need it.

## Adding Pages

Just add a new `your-page-name.md` file in the `_pages` directory. At the top of the file, add this "frontmatter":

```
---
layout: page
title: "your page name"
permalink: /your-page-name
---
```

## Adding Posts

Just add a new `YYYY-MM-DD-your-post-name.md` file in the `_posts` directory. Note that the name of the file will become the URL and you must follow the date convention. At the top of the file, add this frontmatter:

```
---
layout: post
title "Your Post Title"
date: 2021-12-20
---
```