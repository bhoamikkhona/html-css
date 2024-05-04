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
    - [Pseudo-Classes](#pseudo-classes)
    - [Styling Hyperlinks](#styling-hyperlinks)
    - [Using Chrome DevTools](#using-chrome-devtools)
    - [CSS Theory 01: Conflicts Between Selectors](#css-theory-01-conflicts-between-selectors)
    - [CSS Theory 02: Inheritance and the Universal Selector](#css-theory-02-inheritance-and-the-universal-selector)
- [Challenge 01](#challenge-01)
  - [CSS Theory 03: The CSS Box Model](#css-theory-03-the-css-box-model)
  - [Using Margins and Paddings](#using-margins-and-paddings)
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

### Pseudo-Classes

- `:first-child`
- `:last-child`
- `:nth-child(number)`
- `:nth-child(even)`
- `:nth-child(odd)`
- A misconception of how the pseudo-classes work.
- Let's say that we wanted to select the first paragraph element that is inside of the `<article>` in the example below:

```html
<article>
  <header>
    <img src="#" alt="example" />
    <p>lorem ipsum</p>
  </header>
</article>
```

- To do that, you might set the selector like so:

```css
article p:first-child {
  color: red;
}
```

- Now if we check our page, you will that nothing happened.
- The misconception is that this selector: `article p:first-child` should have selected the first `<p>` element inside of the `<article>` which would be `<p>lorem ipsum</p>`.
- Because `<p>lorem ipsum</p>` is the first paragraph inside the article.
- However, this is not how the `:first-child` pseudo class actually works.
- Instead, what CSS will do is to select a `<p>` element that is actually the first-child of the article.
- As of right now `<p>lorem ipsum</p>` is the first paragraph of the article but, it is not the first child of the article. The first child of the article is actually the header.
- If our HTML was set up like so:

```html
<article>
  <p>lorem ipsum dolor</p>
  <header>
    <img src="#" alt="example" />
    <p>lorem ipsum</p>
  </header>
</article>
```

- Then, in this case, the `<p>lorem ipsum dolor</p>` would get the color red because it quite literally is the first child of the article.
- Therefore, this selector `:first-child` does not work in the way that maybe we might think it would. The same thing goes for `:last-child` and `:nth-child()`
- What this means that when we mix multiple elements inside of a parent element, then these pseudo classes don't really work well.
- They are however perfect for situations like a list, where all the child elements are the same i.e. in ordered list or in un-ordered list, all the child elements are supposed to be a `<li>` element so in that case, the `:first-child`, `:last-child`, and `:nth-child()` would work perfectly.
- The pseudo-classes that we just learned are all about matching the existing HTML structure. However, there are also other types of pseudo classes so, let's learn about them in the next lesson.

### Styling Hyperlinks

- Abbreviation LVHA to style links (anchor tags)
  - `:link` - targets elements with `href` attribute
  - `:visited` - after we have visited the link
  - `:hover` - when hovering over the link
  - `:active` - when clicking on the link
- `text-decoration`

### Using Chrome DevTools

- User Agent Stylesheet i.e. default styles

### CSS Theory 01: Conflicts Between Selectors

- ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/79ffeaec-9127-4de1-9c49-77f87de29f98)
- ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/7610fab5-ef22-4559-a42d-229226085fc6)
- Conflicting CSS rules and how they are resolved i.e. which ones get apply onto the element and show on the UI.
- Highest to Lowest Selector Priorities:
  - Declarations marked with `!important` - should not use unless absolutely necessary
  - Inline Styles - should not use, bad practice
  - ID Selectors
  - Class Selector
  - Element Selector
  - Universal Selector

> [!NOTE]
> A class can have the exact same name as an ID, that is not a problem.

> [!NOTE]
> Pseudo classes add to class specificity.

> [!NOTE]
> Instead of using `!important` keyword, try and resolve the CSS by using simpler selectors. `!important` keyword should be the absolute last resort when everything else fails.

### CSS Theory 02: Inheritance and the Universal Selector

- Inheritance is a mechanism by which some styles/properties get their values inherited from parent elements to child elements.
- Not all properties get inherited. The ones that do are mostly about text.
- An inherited property is very easily overwritten by any rule which has a value for that same property. So in a sense, we can say that inherited values are the ones who have the lowest priority.
- Inheritance is not the same as selected each and every element on the body and giving them the style that we declare in their parent element. The inherited styles are simply passed down to children.
- An example of the property that do not get inherited: `border`
- Universal Selector
  - Universal selector basically selects each and every element on a webpage and applies the css styles mentioned to it. It is denoted by `*`.
  - There is no inheritance involved with the universal selector, therefore this is perfect if you want to apply a certain property that does not automatically get inherited to all the elements.
  - Note that Universal selector has the lowest priority i.e. it will easily be override.

# Challenge 01

- CSS Properties:
  - `cursor: pointer`

### CSS Theory 03: The CSS Box Model

- The Box Model defines how elements are displayed on a webpage and how they are sized.
- In a box model, each and every element on a webpage can be seen as a rectangular box, and each of these boxes can have content, a border, and space inside and outside of it.
- Content:
  - This is the actual content of the element.
  - It can be text, images, table, video, etc.
  - Using CSS properties, we can specify both the height and the width of the content area.
- Border:
  - A line around the element, still inside of the element.
- Padding:
  - Invisible space around the content, inside of the element, between the content and the border.
- Margin:
  - Space outside of the element, between elements.
- Fill:
  - Area that gets filled with background color or background image.
- Content + Padding + Border altogether are the visible part of the element. Around that, we can add some margin in order to create space between elements.
- All of these are optional. We don't have to specify them. We can define none of them, or some of them, or all of them. It depends on how we want our layout to look like.
- Finally, there is also something called the fill area. This can be a bit confusing to understand.
- Remember that the text content and images are inside the content box. The same does not apply for background images or the background color of an element. These properties will be applied not only to the content area, but to the entire fill area, which also includes the padding and the border.
- Basically, if we apply a background image or color, it will occupy the entire visible part of the element.
- Element Height and Width Calculation
  - As mentioned before, we can specify the height and the width of the content area.
  - If we choose not to define them, then the box model will simply imply them based on the content.
  - However, the specified or implied heights and widths are actually not the final sized of the element and that's because the border and the padding are also taken into account.
  - Final element width = left border + left padding + width + right padding + right border
  - Final element height = top border + top padding + height + bottom padding + bottom border
  - As you can see, the margin is not part of the width or height calculations of the elements because, it is just space that is around them.
  - As mentioned before, we can specify all these individual sizes using certain CSS properties.
  - It is important to note that this way of calculating heights and widths is actually just the default behavior of the box model.
  - However, we can change this default behavior because it actually doesn't make much sense. We will learn how to do that a bit later.

### Using Margins and Paddings

- An element which has a background color, could always use some padding.
- CSS Properties:
  - `padding` and its shorthands
    - `padding-top`
    - `padding-right`
    - `padding-bottom`
    - `padding-left`
- Global Reset

  - All the elements have default styling attached to them and those make it quite hard for us to style our page.
  - In order to avoid that unnecessary difficulty, we do something called the global reset.
  - Margin and Padding do not get inherited from one element to its child so, we cannot use inheritance for that.
  - Instead, we can use the universal selector which selects all the elements on a webpage and gives them the style we provide.
  - What we do is, we use the universal selector and within that, we set the margin and padding to 0 in order to global reset. This makes sense because the universal selector has a very low priority i.e. it is very easy to over-write it.

> [!NOTE]
>
> When you want to create space between elements, choose one either margin top or margin bottom. Do not mix them.
>
> Margin bottom is more preferable.

> [!NOTE]
>
> After we global reset the webpage, you will notice that if you have any `<ol>` or `<ul>` elements on the page, their bullets will be gone. This because they need left margin to show.

- Collapsing Margins:
  - When we have two margins occupying the same space, only one of them is actually visible on the appage; and usually, the one visible is the larger of the two.

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
