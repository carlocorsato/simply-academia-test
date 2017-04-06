---
layout: post
title: Links & Buttons
permalink: /links&buttons/
excerpt: "All you need to create links and buttons"
date: 2017-03-08 12:00
modified: 2017-03-08 12:00
categories:
  - text-formatting
  - syntax
tags:
  - text-formatting
  - syntax
author: carlo_corsato
share: true
---

{% include toc-box title="Text Formatting" icon="pencil" %}


## Inline Links {#inline-links}

Links, including inline links, have two parts:

1. linking text
2. link url

Kramdown offers minimal syntax for combining both in one string:

```bash
[linking tex](link url)
```

E.g.
Within [] you can still use [*text* <u>attributes</u>](#text-attributes) such as italic or underlined words to style your text. Here below how it looks your syntax with an [anchor link](#anchor-links) included or with an url.

```html
E.g.
Within [] you can still use [*text* <u>attributes</u>](#text-attributes) such as italic or underlined words to style your text. Here how it looks your syntax with an [anchor link](#anchor-links) included or with an url.

Learn more from [Kramdown documentation](https://kramdown.gettalong.org/syntax.html#ordered-and-unordered-lists).
```

<br>
Learn more from [Kramdown documentation](https://kramdown.gettalong.org/syntax.html#ordered-and-unordered-lists).

---

## Anchor Links {#anchor-links}

To include anchor links to your pages, articles and posts you need to:

<a id="anchor-links-options"></a>
* add an `id` to your headers

* add an `id` to any paragraph of a text you like to link to


##### Headers-ID

Kramdown supports Header IDs:

```bash
## YourHeader {#YourID}
e.g. ## Anchor Links {#anchorlinks}
```

To direct your link to a header, use the usual markdown syntax for links -- `[]()`:

* With only ```(#YourID)``` when linking to a header-id within the same page:
e.g. [Linking text to my Header Anchor Links](#anchor-links)

```html
With only ```#YourID``` when linking to a header-id within the same page:
e.g. [Linking text to my paragraph Anchor Links](#anchor-links)
```

* With the path-to-the-folder (or the permalink) of the page/article/post where your header-id is located -- ```(path-to-the-folder or permalink/#YourID)``` -- when linking to a header-id on a different page:
e.g. [Linking text to my Header Anchor Links](/text-formatting/#anchor-links)

```bash
With the path-to-the-folder (or the permalink) of the page/article/post where your header-id is located -- ```(path-to-the-folder or permalink/#YourID)``` -- when linking to a header-id on a different page:
e.g. [Linking text to my Header Anchor Links](/text-formatting/#anchor-links)
```

It is good practice to include IDs to your headers, especially those introducing to key or recurrent topics, in order to make easier direct links to specific sections of your site.
{: .notice}

##### Paragraphs-ID

You have to use `<a id>` immediately before ` the paragraph you like to link to:

```html
<a id="YourID"></a>
YourParagraph with YourText
```

whilst the proper anchor link works with the usual markdown syntax `[]()`.

When linking to a paragraph-id within the same page:

```bash
[Your Text with a link](#YourParagraph-ID)
```

but when linking to a header-id on a different page:

```bash
[Your Text with a link](/path-to-the-folder or permalink/#YourParagraph-ID)
```

E.g.
Let's say I want to link straight to my above list with the two anchor link options:

Here it is my paragraph in kramdown:

```bash
<a id="anchor-links-options"></a>
* add an `id` to your headers

* add an `id` to any paragraph of a text
```
And here it is a sample text linking to my paragraph:
[See above anchor link options](#anchor-links-options)

```bash
[See above anchor link options](#anchor-links-options)
```

---

## Buttons {#buttons}

To include a Button linking to a page/article/post or a different website, you need to type:

```bash
<div markdown="0"><a href="{{ site.url }}/path-to-the-folder / or the url of a website" class="btn2">Text to display on the button</a></div>
```

E.g.
A button to learn more about Kramdown syntax:

<div markdown="0"><a href="https://kramdown.gettalong.org/documentation.html" class="btn2">Learn more about Kramdown</a></div>

```html
<div markdown="0"><a href="https://kramdown.gettalong.org/documentation.html" class="btn2">Learn more about Kramdown</a></div>
```

<div markdown="0"><a href="https://kramdown.gettalong.org/documentation.html" class="btn">Learn more about Kramdown</a></div>

```html
<div markdown="0"><a href="https://kramdown.gettalong.org/documentation.html" class="btn">Learn more about Kramdown</a></div>
```

To include a transparent button (turning to black when hovering) you will apply `class="btn2"`, whilst to get the opposite colour mix type in `class="btn"`.

**Note:** Previous/Next buttons are automatically generated at the bottom of each article/post.
{: .notice}

---
