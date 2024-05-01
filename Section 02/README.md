# Section 02: HTML Fundamentals

**About:** In this section, we will learn the fundamental language of web developmentm which is HTML. You will learn about the most important HTML elements such as headings, paragraphs, lists, images, links, and more.

## Lessons Learned

### Introduction to HTML

- What is HTML?
  - HTML stands for <ins>HyperText Markup Language</ins>.
  - It is one of the core technologies of web development, along with CSS and JavaScript.
  - It is a markup language that we (web developers) can use to structure and describe the entire content of any webpage.
    - NOTE that it is a markup language and not a programming language.
    - It is a markup language because we use it describe something and in the case of HTML, we do describe content using elements.
  - In HTML, we use different elements to describe different types of content e.g. paragraphs, links, headings, images, videos, etc.
  - Web browsers, such as Google Chrome, can understand HTML and render HTML code as websites.
- Anatomy of an HTML Element
  - An HTML element is usually made up of 3 parts viz:
    - Opening Tag
    - Content or Child Element
    - Closing Tag
  - Some elements such as images have no content at all - they only have an opening or a self-closing tag.

### HTML Document Structure

- `<!DOCTYPE html>`
  - This is the doc type. This will let the browser know that we are using HTML in this file and all browsers will then know that they should use the HTML 5 specification to render this HTML.
- `<html></html>`
  - This contains the head and body tags.
- `<head></head>`
  - The head element is basically for things that are not visible in the browser window.
- `<body></body>`
  - The body is for all the elements that is visible on the page.
- `<title></title>`
  - This displays the title on the tab of the browser.
- Indentation and code structure

### Text Elements

- Headings
  - The goal of heading is to break up big block of text into more logical sections, and to add a title to each sections.
  - There are 6 different headings i.e. there is an hierarchy of headings so that we can establish a hierarchy in our text.

```html
<h1>heading 1</h1>
<h2>heading 2</h2>
<h3>heading 3</h3>
<h4>heading 4</h4>
<h5>heading 5</h5>
<h6>heading 6</h6>
```

> [!NOTE]
> Each and every webpage should only have one h1 heading i.e. only one primary heading. This is very important to keep in mind. This is not really mandatory i.e. it does not violate any HTML rules if we have multiple h1s, but it is a good practice to always just have one of them. The other ones, we can have multiple of them.

- `<!-- comment -->` HTML Comments
- `<b></b>` - Bold text
- `<strong></strong>` - Bold text (use this instead of `<b>` due to semantic meaning)
- `<i></i>` - Italic text
- `<em></em>` - Italic text (use this instead of `<i>` due to semantic meaning)

### More Text Elements: Lists

- The concept of Child elements and Parent elements.
- `<ol></ol>` - Ordered List
- `<ul></ul>` - Unordered List
- `<li></li>` - List Item

### Images and Attributes

- Attributes
  - Attributes are basically pieces of data which we can use to describe elements.
- `<img src="" alt="" />`
  - `src` attribute
    - The source (path) of the image
  - `alt` attribute
    - `alt` stands for alternative text.
    - It is imperative to always use it and never skip this tag for various important reasons. One of them is that it will allow search engines such as Google Chrome, to actually know what is in the image, because without this description, search engines don't really have a way of knowing what the image is actually about.
    - The second and probably even more important is that by specifying the description of the image, we are also allowing blind people (people who use screen reader - the screen reader will read the image description to them) to use the website.
    - The third reason is that if the image is no longer available or the path mentioned in the `src` attribute is wrong, the browser will display the `alt` text instead.
  - `width`
  - `height`
- `<html lang="en"></html>`
  - `lang` attribute on html tag. It specifies the language that we use for the webpage.
- `<meta charset-"UTF-8" />` (self-closing)
  - The meta tag is used for meta data which is essentially data about data.
  - We set its attribute `charset` to "UTF-8" which is simply all the simple characters that we use in the English Language.

### Hyperlinks

- One of the fundamental building blocks of the internet are hyperlinks, or for short, links.
- Links are what actually enables the internet to be a worldwide web.
- Without links between pages, there would be no web.
- We can place links into two big categories.
  - The first category is links that point to other pages within our own website.
  - The second category is links that point to outside of our website.
- Anchor tags
  - `<a href="#"></a>`
    - `href` attribute
      - What makes an anchor element really a link is the `href` attribute.
      - Without the `href`, the anchor will be unclickable.
    - `target="_blank"` - opens the link on a new tab.

### Structuring our Page

- Container Elements
  - `<nav></nav>`- Stands for navigation
  - `<header></header>` - Top part of the page
  - `<article></article>`
  - `<footer></footer>`
- HTML entities
  - `&copy;` - copyright symbol

### A Note on Semantic HTML

- In HTML, when we talk about semantics, what we mean is that certain elements have actually a meaning or a purpose attached to them.
- So, when we think about a certain HTML element, we should not think about what that element looks like as it is rendered on the page but instead, we should think about what that element actually means and what it stands for.
- That is basically the definition of semantic HTML.
- Not all elements in HTML are semantic.
  - e.g. `<b>` vs. `<strong>` elements
- `<div></div>` - creates a box without any meaning i.e. no semantics.
  - We should only use div element when we don't want to attach a certain meaning to a container.
- Why use semantic HTML?
  - Search engine optimization - it means that search engines such as Google will be able to understand the structure of your content, and therefore, they will be able to better analyze what your content and what your webpage is all about.
  - Also, writing semantic HTML is extremely important for accessibility, and especially for people who rely on screen readers to consume our webpages.
  - Essentially, when we think about HTML, we should not only think about how it actually looks like in the browser but even more about what these elements actually mean and what they stand for.

### Challenge 01

- `<aside></aside>`

### Challenge 02

- `<button></button>`
- HTML Entities
  - `&rarr;`

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
