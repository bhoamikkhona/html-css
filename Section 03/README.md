# Section 03: CSS Fundamentals

**About:** In this section we will learn about the basics of CSS. CSS is essentailly all about styling the content that we write in HTML. We will keep building on our project from last section to add some visual styles to it along with learning some theoretical concepts that are behind CSS for deeper understanding.

## Table of Content

- [Section 03: CSS Fundamentals](#section-03-css-fundamentals)
  - [Table of Content](#table-of-content)
  - [Lessons Learned](#lessons-learned)
    - [Introduction to CSS](#introduction-to-css)
    - [Inline, Internal, and External CSS](#inline-internal-and-external-css)
    - [Styling Text](#styling-text)
    - [Combining Selectors](#combining-selectors)
    - [Class and ID Selectors](#class-and-id-selectors)
  - [Author](#author)

## Lessons Learned

### Introduction to CSS

- What is CSS?
  - CSS stands for Cascading Style Sheets.
  - It is one of the core technologies of the web.
  - We use CSS to describe the visual style and the presentation of the content that we previously wrote using HTML.
  - CSS consists of countless properties that us (developers) can use to format the content of the webpage, e.g. font, text, spacing, layout etc.
- Anatomy of CSS Declaration
  - ![CSS Rule](https://github.com/bhoamikkhona/html-css/assets/143898153/12c6af9e-050b-4847-8c29-118a18a79cdc)
  - A CSS Rule
    - Selector
    - Declaration Block
      - Declaration/Style
        - Property
        - Value
  - In the end, our CSS code will be a lot of different CSS rules one after another where we select all of our elements and style them in any way that we want.

### Inline, Internal, and External CSS

- There are 3 places where we can write CSS, we call them:
  - Inline CSS
    - Inline styles should never be used.
  - Internal CSS
    - `<style></style>`
  - External CSS
    - Linking an external CSS file to HTML file: `<link rel="stylesheet" href="./style.css" />`
- CSS Properties:
  - `color`
- A brief introduction to the concept of separation of concerns.

### Styling Text

- CSS Properties:
  - `font-size` - default font-size is 16px
  - `font-family`
  - `text-transform`
  - `font-style`
  - `line-height` - we specify its value without a unit
  - `text-align`
- A brief introduction to the concept of inheritance.

### Combining Selectors

- List Selector: Creating a list of selectors to apply a common style, eg:

```css
h1,
h2,
h3,
h4,
p,
li {
  font-family: sans-serif;
}
```

- Descendant Selector: Selecting all the particular child elements of a particular parent element. eg: Selecting all the `<p>` elements inside a `<footer>` element.

```css
footer p {
  font-size: 16px;
}
```

### Class and ID Selectors

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
