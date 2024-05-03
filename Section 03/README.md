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
    - [Working with Colors](#working-with-colors)
      - [RGB Model](#rgb-model)
      - [Defining Colors in CSS](#defining-colors-in-css)
      - [CSS Properties](#css-properties)
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

- CSS Comments
- ID Selector

```css
#author {
  font-style: italic;
}
```

- Class Selector

```css
.related-author {
  font-size: 18px;
}
```

- The big difference between ID and Class is that we are not allowed to repeat ID names. In other words, we can only use each ID name only once.
- If we need to re-use a name multiple times then we need to use classes for that.
- CSS uses kebab case.
- CSS Properties:
  - `font-weight`
  - `list-style`

> [!NOTE]
> In the real world, we never use IDs; we always use classes. This is because, by using classes, we are prepared for the future.
>
> Imagine that we used a list and gave it an ID of "related." Then, sometime later down the road, we wanted to add another list of related posts. At this point, we would have to go back and change the ID to a class so that we could have another element with the same styling without repeating those styles.
>
> This would also prevent bugs, considering if we missed one of the CSS rules when converting it from an ID to a class.

### Working with Colors

- There are many ways of representing colors in computers i.e. writing them in code but, one of the more traditional models is the RGB model.

#### RGB Model

- In the RGB model, every single color can be represented by any combination of red, green, and blue colors.
- In order to represent a certain color, we need to give each of the three base colors any value between 0 and 255. With that, we can define a total of 16.8 million different colors.
- Red: rgb(255, 0, 0)
- Green: rgb(0, 255, 0)
- Blue: rgb(0, 0, 255)
- All the colors at 255 gives us white and all the colors at 0 give us black.

#### Defining Colors in CSS

- In CSS, we have 2 ways of writing colors using the RGB model and those are the RGB notation and Hexadecimal notation.
  - RGB notation example: rgb(238, 68, 67)
  - Hexadecimal notation example: #ee4443 (r = ee, g = 44, b = 43)
    - Hexadecimal numbers go from 0 to ff (255 in hexadecimal numbers)
    - Hexadecimal shorthand, eg #0ff;
- RGB with Transparency: rgba(238, 68, 67, 0.3) - `a` is called alpha which denotes the opacity of the color.
- In practice, we mostly use the hexadecimal notations and if we need transparency, we use rgba() function.
- Shades of Grey
  - When colors in all 3 channels are the same, we get a grey color.
  - There are 256 pure greys to choose from.

#### CSS Properties

- `color`
- `background-color`
- `border` - it accepts multiple values because it is short-hand property
  - `border-top`
  - `border-right`
  - `border-bottom`
  - `border-left`

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
