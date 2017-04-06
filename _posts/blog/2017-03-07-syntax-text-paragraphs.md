---
layout: post
title: Paragraphs
permalink: /paragraphs/
excerpt: "All you need to create your paragraphs"
date: 2017-03-07 12:00
modified: 2017-03-07 12:00
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

## Paragraphs {#paragraphs}

To create a paragraph you just need to click enter twice and separate your text:

E.g.

Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.

Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu. In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium.

```bash
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa quis enim.

Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu. In enim justo, rhoncus ut, imperdiet a, venenatis vitae, justo. Nullam dictum felis eu pede mollis pretium.
```

---
##### Breaks {#text-breaks}

To add enter line breaks, you can use the usual ```<br>``` tag o simply leave a blank line as in the above example.

For thematic break separators you use the usual ```<hr>``` tag or just type three dashes `---` to adopt the simple kramdown syntax. Separators can be included everywhere in the text.

E.g.
###### Your Header
---
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et<br> Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
<hr>
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. <br><br>
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor.
<br>
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor.
<hr>

```html
E.g.
###### Your Header
---
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et<br> Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
<hr>
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. <br><br>
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor.
<br>
Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor.
<hr>
```

**Note:** While ```<br>``` works as an inline tag (straight after the text), ```<hr>``` must be on a separate line with no other text before or after the tag.
<br><br>In the example we have a mix of kramdowm ad html, however the simple use of kramdowm is more advisable. Use html only for writing [notices](#notice).
{: .notice-warning}

---

##### Ordered and Unordered List {#list}

Kramdown offers a very simple syntax for both ordered and unordered lists:

Eg.
* kram
+ down
- now

1. kram
2. down
3. now


```bash
* kram
+ down
- now

1. kram
2. down
3. now
```

For more details (including indentations and sublists) see [Kramdown documentation](https://kramdown.gettalong.org/syntax.html#ordered-and-unordered-lists)


##### Blockquotes {#blockquotes}

To add a blockquote you only need to include `>` right before your text:

> Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus. Nullam quis ante. Etiam sit amet orci eget eros faucibus tincidunt.

```bash
> Maecenas nec odio et ante tincidunt tempus. Donec vitae sapien ut libero venenatis faucibus. Nullam quis ante. Etiam sit amet orci eget eros faucibus tincidunt.
```

---

##### Notice {#notice}

Adding notices to your text couldn't be easier: include `{: .include}` in the line immediately after the paragraph you want to box in.

Example:

This is a notice
{: .notice}

```bash
This is a notice
{: .notice}
```

If you need to include a warning notice with a redish background, you simply need to include ```{: .include-warning}``` in the line immediately after the paragraph you want to box in.

Example:

This is a warning notice
{: .notice-warning}

```bash
This is a warning notice
{: .notice-}
```

Text can be formatted as it was a plain paragraph, adding attributes, links, etc.

Example:

This **is** a <u>warning</u> *notice* with **bold**, <u>underlined</u> and *italic* text.
{: .notice-warning}

---
