---
layout: post
title: Text Attributes
permalink: /text-attributes/
excerpt: "All you need to write a text"
date: 2017-03-06 12:00
modified: 2017-03-06 12:00
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

## Text Attributes {#text-attributes}
---

##### Bold

Simply add ** before and after your text: this is **bold**

```bash
Simply add ** before and after your text: this is **bold**
```

---

##### Italic

Simply add * before and after your text: this is *italic*

```bash
Simply add ** before and after your text: this is *italic*
```

---

##### Underlined

Usual `u` tag for <u>underlined text</u>.

```html
Usual `u` tag for <u>underlined text</u>.
```

---
##### Deleted

Usual `del` tag for <del>deleted text</del>.

```html
Usual `del` tag for <del>deleted text</del>.
```

---

##### Subscripted and Superscripted {#subscripted-superscripted-text}

Usual `sub` and `sup` tags for <sub>subscripted</sub> or <sup>superscripted</sup> text.

```html
Usual `sub` and `sup` tags for <sub>subscripted</sub> or <sup>superscripted</sup> text.
```

---

##### Uppercase & Small Caps {#uppercase-smallcaps}

Uppercase text goes with simple liquid syntax following the paragraph to modify

```liquid
{: .all-caps}
```

E.g.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.
{: .all-caps}

```bash
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.
{: .all-caps}
```

Similar syntax for Small Caps:

```liquid
{: .small-caps}
```

E.g.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.
{: .small-caps}

```bash
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.
{: .small-caps}
```

---

##### Hearders {#headers}

You can have 6 levels (from bigger to smaller) simply adding 1 to 6 # before your header:

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

```bash
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
```

---

##### Footnotes {#footnotes}

To add a footnote is need to type `[^number-of-the-note]` where you need it to be included. At the bottom of the same paragraph you then type in `[^number-of-the-note]: text for your footnotes`. Footnotes will be display at the bottom of your articles/post.

**Note:** you may wish to include `---` at the very bottom of your text to generate a break separator.
{: .notice}

E.g.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit.[^1] Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.[^2] Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate


[^1]: See Corsato 2017, p. xy.
[^2]: http://www2.le.ac.uk/library/help/referencing/footnote

```bash
Lorem ipsum dolor sit amet, consectetuer adipiscing elit.[^1] Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.[^2] Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate

[^1]: See Corsato 2017, p. xy.
[^2]: http://www2.le.ac.uk/library/help/referencing/footnote


# add --- at the bottom of your text to get a break separator, your footnotes will follow immediately after your article/post otherwise.
---
```
---
