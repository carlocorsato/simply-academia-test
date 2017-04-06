---
layout: post
title: Table of Contents
permalink: /toc/
excerpt: "All you need to generate tables of contents"
date: 2017-03-09 12:00
modified: 2017-03-09 12:00
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


## Table of Contents {#inline-links}

Tables of contents (ToCs) are generated automatically by Kramdown with a simple markup:

```bash
- TOC
{:toc}
```

All the headings in pages/article/posts will be all automatically included in the ToC, except for those we don't want to. For the latter, we apply the class `no_toc`, and Kramdown will skip those headings:

```bash
### This heading will be included in the ToC

### This heading will not be included in the ToC.
{: .no_toc}
```

Of course, we can make the ToC an ordered list instead of unordered:

```bash
1. TOC
{:toc}
```

**Pro-tip:** The theme generates ToC as unordered list. If you need ToCs with ordered lists you have to create a modified `toc` file (e.g. `toc-ordered`) in the `_includes`.
{: .notice}

<br>
You can create your ToCs in three different styles: Simple; Hidden; Boxed.


#### Simple



---

#### Hidden

---

#### Boxed


---
