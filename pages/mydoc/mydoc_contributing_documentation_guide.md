---
title: Documentation Guide
sidebar: mydoc_sidebar
tags: [documentation]
keywords: getting_started
last_updated: April 7, 2022
permalink: mydoc_contributing_documentation_guide.html
folder: mydoc
summary: You can include a summary!
---
## Site source
This site is based on [this site](https://idratherbewriting.com/documentation-theme-jekyll/index.html).

## Markdown
This site uses `kramdown`, which may be slightly different from the markdown syntax you expect.


## Highlight Options
You can add different highlights to draw attention to different types of significant notes.

{% include note.html content="Test note. <a href='https://cmu-cloud-lab.github.io/index.html'>Link goes here</a>." %}

{% include important.html content="Test important." %}

{% include warning.html content="Test warning." %}

{% include tip.html content="Test tip." %}


## Code
You can include code, and make it easy for users to copy that code for their own use!

{% include code_header.html %}
```bash
ls -l
```

{% include code_header.html %}
```bash
ls -la
```

{% include links.html %}
