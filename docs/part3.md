---
title: "Part 3 - Markup languages"
permalink: /part3/
nav_order: 3
published: true
---

# Markup languages

*"In computer text processing, a markup language is a system for annotating a document in a way that is syntactically distinguishable from the text, meaning when the document is processed for display, the markup language is not shown, and is only used to format the text. The idea and terminology evolved from the 'marking up' of paper manuscripts (i.e., the revision instructions by editors), which is traditionally written with a red or blue pencil on authors' manuscripts. Such 'markup' typically includes both content corrections (such as spelling, punctuation, or movement of content), and also typographic instructions, such as to make a heading larger or boldface."* [**Wikipedia**](https://en.wikipedia.org/wiki/Markup_language)

Markup languages are not coding languages, even though they have quite similar features. Markup languages are widely used in creating documentation, and that is why we also need to know something about them. Some markup languages are also used in for example system configuration, and you might have written some already without knowing about it. Let's take a look at few of them.

## HTML

HTML is often referred to as a programming language, which is technically not true. It is a markup language, describing the structure of a document. HTML comprises a set of elements and tags used to define and show different sections of the document, also giving them specific functionalities. Tags can for example turn a word into a link, make it cursive, or change its size.

Here is an example of an HTML element:

```html
<p>This is a piece of text.</p>
```

Let’s look at the structure of the element. An HTML element is composed of three parts:

1. The start tag *\<p\>*
2. The content itself This is a piece of text
3. The end tag *\<\/p\>*

HTML tags are keywords hidden inside the site, but not shown to the end user by the browser. They define how the browser styles and shows the contents of the document the user is viewing. There are countless different HTML tags, each serving to create specific kinds of elements. We’ll start with the elements used to edit text.

1. *\<h1\>\<\/h1\>*: This tag is used to create heading elements. There are six different heading tags, ranging from h1 to h6. The primary heading is created using the first tag h1. The least important heading is created with h6.
2. *\<p\>\<\/p\>*: The element created with the tag p contains the body text of the document.
3. *\<em\>\<\/em\>*: The text inside an element created with the tag em is shown in cursive.
4. *\<strong\>\<\/strong\>*: The text inside an element created with the tag strong is shown in bold. You can also create elements with \<b\> and \<i\> to show text in bold and cursive respectively.


With these, we can create even static web page. Let's start with a little less ambitious project, and have ourselves a piece of code:

```html
<h1>This is the header</h1>

<p>This is a <strong>sentence</strong>.</p>

<p>This is a <b>bold</b> and <i>recursive</i> sentence.</p>
```

If we take this into a file and open in it oor web browser, we will get a view like this:

![First html](https://github.com/centria/design-and-documentation/raw/master/assets/images/part3/html.jpg)

## MarkDown

## XML and YAML

## TeX