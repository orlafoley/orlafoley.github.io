---
layout: page
title: Markdown Guide
permalink: /markdown-guide/
---

Welcome to the **Markdown Syntax Guide**! This guide will walk you through some common Markdown features with examples using the `code snippets` feature.

---
## 1. Headings
In Markdown, headings are created using the `#` symbol.

{% highlight markdown %}
## Heading 1
### Heading 2
# Heading 3
{% endhighlight %}

This will render as:

## Heading 1
### Heading 2
# Heading 3

---
## 2. Bold and Italic Text
To make text bold or italic, use `**` for bold and `*` for italic.

{% highlight markdown %}
**This text is bold.**  
*This text is italic.*
{% endhighlight %}

this will render as:

**This text is bold.**  
*This text is italic.*


---
## 3. Lists
Unordered Lists
Use `-`, `+`, or `*` to create an unordered list.

{% highlight markdown %}
- Item 1
- Item 2
  - Sub-item 1
  - Sub-item 2
{% endhighlight %}

This will render as:  

- Item 1
- Item 2
  - Sub-item 1
  - Sub-item 2


Ordered Lists use numbers followed by a period for ordered lists.  

{% highlight markdown %}
1. First item
2. Second item
   1. Sub-item 1
   2. Sub-item 2
{% endhighlight %}

This will render as:  
1. First item
2. Second item
   1. Sub-item 1
   2. Sub-item 2


---
## 4. Links
To create a link, follow the below example's format.

{% highlight markdown %}
[GitHub](https://github.com)
{% endhighlight %}

This will render as: [GitHub](https://github.com)


---
## 5. Images
Images are similar to links. Each link has an "alt text". This is the text that appears when you hover over the image.

{% highlight markdown %}
![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)
{% endhighlight %}

The above example (a link to the GitHub Logo) renders as:

![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)


---
## 6. Blockquotes
Use `>` to create a blockquote.

{% highlight markdown %}
> This is a blockquote.
{% endhighlight %}

This will render as:

> This is a blockquote.


---
## 7. Tables
Tables are created using pipes `|` and hyphens `-` to separate columns and rows.

{% highlight markdown %}
| Header 1 | Header 2 |
|----------|----------|
| Row 1    | Data 1   |
| Row 2    | Data 2   |
{% endhighlight %}

This renders as:

| Header 1 | Header 2 |
|----------|----------|
| Row 1    | Data 1   |
| Row 2    | Data 2   |


---
## 8. Checkboxes
You can create checkboxes using `- [ ]` for an unchecked box and `- [x]` for a checked box.

{% highlight markdown %}
- [x] Task 1
- [ ] Task 2
{% endhighlight %}

This will render as:
- [x] Task 1
- [ ] Task 2
