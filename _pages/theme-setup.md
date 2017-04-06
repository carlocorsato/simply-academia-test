---
layout: page
permalink: /theme-setup/
title: Theme Setup
excerpt: "Instructions on how to install and customize the Jekyll theme So Simple."
modified: 2016-09-12T08:42:37-04:00
image:
  feature: gears.jpg
  credit: Peter Chong
---

General notes and suggestions for customizing **Simply Academia**.

{% include toc-box title="Setup" icon="cogs" %}

## Installation {#toc}

Simply Academia requires [Jekyll](http://jekyllrb.com/) 3.0. Make sure to run `bundle update` if you aren't on the latest version to update all gem dependencies.

To create a new Jekyll site using Simply Academia you should:

1. Fork the [Simply Academia Theme](http://github.com/mmistakes/so-simple-theme/fork) on your [GitHub account](https://github.com). <br> PS: if you don't have a Github account (see [further instructions](http://www.wikihow.com/Create-an-Account-on-GitHub)).
2. Clone the repository you just forked and rename it.
3. [Install Bundler](http://bundler.io) `gem install bundler` and Run `bundle install` to install Jekyll and all dependencies.
4. Update `_config.yml` in the root folder, and edit `navigation.yml` in the folder `_data`.
5. Replace demo posts and pages with your own in the folders `_posts` and `_pages`). Full details below.

To use Simply Academia with an existing Jekyll, then you have to:

1. [Download Simply Academia](https://github.com/mmistakes/so-simple-theme/archive/master.zip) and unzip.
2. Rename `simply-academia-theme-master` to something meaningful ie: `my-new-site`
3. Run `bundle install` to install Jekyll and all dependencies.
4. Update `_config.yml` in the root folder, and edit `navigation.yml` in the folder `_data`.
5. Replace demo posts and pages with your own in the folders `_posts` and `_pages`). Full details below.

**Pro-tip:** if you are running your site on GitHub, keep it on the `master` branch for user/organisation pages, or create the `gh-pages` branch for project pages hosted in a subfolder of your user/organisation account (e.g. carlocorsato.github.io/simply-academia).
{: .notice}

---

## Running Jekyll

The preferred method for running Jekyll is with `bundle exec`, which is all you need if you using GitHub Pages for your site.

> In some cases, running executables without bundle exec may work, if the executable happens to be installed in your system and does not pull in any gems that conflict with your bundle.
>
>However, this is unreliable and is the source of considerable pain. Even if it looks like it works, it may not work in the future or on another machine.

```bash
bundle exec jekyll build

bundle exec jekyll serve
```

**Note:** To get your [Google Analytics]() to show up only in the production environment when using a hosting provider or building your site locally, you will need to prefix the build command with `JEKYLL_ENV=production`
{: .notice}

```bash
JEKYLL_ENV=production bundle exec jekyll build
```


---

## Scaffolding

How So Simple is organized and what the various files are. All posts, layouts, includes, stylesheets, assets, and whatever else is grouped nicely under the root folder. The compiled Jekyll site outputs to `_site/`.

```bash
simply-academia-theme/
├── _data/
     ├── authors.yml             # profiles for authors in your posts
|    ├── navigation.yml          # add/remove items from your navbar
├── _includes/
|    ├── browser-upgrade.html    # prompt to install a modern browser for < IE9
|    ├── disqus-comments.html    # Disqus comments script
|    ├── feed-footer.html        # post footers in feed
|    ├── footer.html             # site footer
|    ├── head.html               # site head
|    ├── navigation-home.html    # site top navigation (homepage)
|    ├── navigation-page.html    # site top navigation (pages / posts)
|    ├── open-graph.html         # meta data for Open Graph and Twitter cards
|    ├── read-time.html          # generated read time (posts)
|    └── scripts.html            # site scripts
├── _layouts/
|    ├── page.html               # single column page layout
|    └── post.html               # main content with sidebar for author/post details
├── _pages/                      # MarkDown formatted pages (including the homepage)
├── _posts/                      # MarkDown formatted posts
├── _sass/                       # Sass stylesheets
├── assets/
|    ├── css/                   
|    |    ├── main.scss          # main stylesheet file
|    ├── your-font-folder/       # include here the folder with your own webfont
|    ├── fonts/                  # webfont (Font Awesome)
|    ├── icons/                  # icons (including favicon)  
|    ├── images/                 # # images for posts and pages (including logos)
|    └── js/
|        ├── _main.js            # main JavaScript file, plugin settings, etc
|        ├── plugins/            # scripts and jQuery plugins to combine with _main.js
|        ├── scripts.min.js      # concatenated and minified _main.js + plugin scripts
|        └── vendor/             # vendor scripts to leave alone and load as is
├── 404.md                       # 404 page
├── feed.xml                     # Atom feed template
└── theme-setup/                 # theme setup page. safe to remove
```

---

## Site Setup

For an introduction or explanations of the `config.yml` file, and more in general for instructions on basic setup, [Michael Rose](https://mademistakes.com) provided everything you may need in the documentation for [So Simple](https://mmistakes.github.io/so-simple-theme/theme-setup/) (section: site setup) and [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/docs/configuration/) (section: configuration).

Simply Academia includes three extra features, you can tweak on your `config.yml` file:

* [*Read time*]() -- default setup 180 words a minute against the recommended average of 200 w/m (I have assumed that scholarly contents might take a bit longer to be read)

* [*Permalink*]() -- default setup `/:categories/:title/`

* [*Timezone*]() -- you can add time and timezone to the date of your posts and articles.
  Type in your timezone. Check out [Wikipedia TZ List](http://en.wikipedia.org/wiki/List_of_tz_database_time_zones).

---

## Adding New Pages, Articles or Posts

Pages, articles and posts are stored respectively in the `_pages`, `_posts/articles`, `_posts/blog` directories. While pages requires a short and meaningful name (e.g. `home`, `about`, etc.), articles and posts should be named according to the `YEAR-MONTH-DAY-title.MARKUP` format as per [the usual](https://jekyllrb.com/docs/posts/).

**Pro-tip:** to streamline the creation of posts and pages, [Jekyll::Compose](https://github.com/jekyll/jekyll-compose) and [Octopress](https://github.com/octopress/octopress) are great plugins you can install to automate this process.
{: .notice}

To create new pages, articles and posts if you have never used markdown files before, you can simply duplicate and rename [*default-page.md*](/default-page), [*2017-01-01-default-article.md*](/default-article) or [*2017-02-02-default-post.md*](/default-post).

---

## Layouts and Content

The theme comes with three layouts:

* `post` for your articles and posts

* `page` for your pages

* `home` for your homepage, which is a version of `page` with some tweaks in the musthead

Layouts are stored in `_layouts`.

**Note:** You need a text editor, such ad [Atom](https://atom.io) ![Atom]({{ site.url }}/assets/icons/atom.png), to create your pages, articles and post.
{: .notice}

---

#### Post and Page

The two main layouts are very similar. Both include the responsive scroll to the top button and allow for large feature images at the top, categories and in the YAML front matter, and optional Disqus comments.

`post` also includes additional features:

* author: the author of your articles and posts (e.g. you or any other contributor)

* read time: calculates how long it takes to read your articles and post

* date and modified date: shows when your articles and posts were created and last modified

* link-post type: creates link-posts/articles

* social share links: includes the social share links you have set up in the `config.yml`

* twitter cards

To learn more about how to use all these feature, please check out [So Simple](https://mmistakes.github.io/so-simple-theme/theme-setup/) and [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/docs/docs-2-2/) documentation.
{: .notice}

---

#### Colours and Typography

Colours and Typography are set in `_sass/_variables.scss` and you can simply change their values to use a different font family or font colour, and a different background colour, etc.

Simply Academia partially follows the style of [Tufte CSS](https://edwardtufte.github.io/tufte-css/) but you can choose whatever style you like most.

---

#### Formatting

Especially if you're not familiar with html, kramdown or css, you might need some help to format and style your pages, articles and posts. Browse to the basics you may need for:

* [Text Formatting]({{ site.url}}/text-formatting)

* [Embed Images & Videos]({{ site.url}}/images&videos)

---

#### Jekyll search

It is a very basic way for [indexing your Jekyll site](https://github.com/mathaywarduk/jekyll-search) and returning search results with JSON.

**Note:** if you need more refined search results you may wish to add [Google Custom Search Engine](https://github.com/brint/jekyll-google_cse).
{: .notice}

To exclude posts/pages from search results add `search_omit: true` to their YAML Front Matter.

---

## Questions?

Found a bug or are in trouble with using the theme for your project/site? Just ping me on Twitter [@CarloCorsato](https://twitter.com/CarloCorsato), drop a private message on Facebook [Carlo Corsato](https://www.facebook.com/carlo.corsato) or [file a GitHub Issue](https://github.com/carlocorsato/simply-academia/issues/new). And if you make something cool with this theme feel free to let me know.

---

## License

This theme is free and open source software, distributed under the MIT License. So feel free to use this Jekyll theme on your site without linking back to me or including a disclaimer.
