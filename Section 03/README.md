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
    - [Adding Dimensions](#adding-dimensions)
    - [Centering our Page](#centering-our-page)
    - [CSS Theory 04: Types of Boxes](#css-theory-04-types-of-boxes)
    - [CSS Theory 05: Absolute Positioning](#css-theory-05-absolute-positioning)
    - [Pseudo-Elements](#pseudo-elements)
    - [Developer Skill 01: Googling and Reading Documentation](#developer-skill-01-googling-and-reading-documentation)
    - [Developer Skill 02: Debugging and Asking Questions](#developer-skill-02-debugging-and-asking-questions)
    - [Challenge 03](#challenge-03)
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

### Challenge 01

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

### Adding Dimensions

- Using `height` and `width` css properties on images.
- Using % instead of px
  - The percentage is usually the percentage of the element's parent container.

### Centering our Page

- There is a simple trick to center the entire page in the browser. Let's learn how.
  - The very first thing that we need to do in order to pull off this trick is to put all of our content into a container element, because otherwise, if we don't do that, then what is there actually to center in the window?
  - In other words, all the children elements take up 100% of their parent's width. When we don't have a container, we essentially are taking the entire body as the parent. Therefore we need a container.
  - Then, set a width of that container, e.g. 700px and then using the property `margin: 0 auto` to center that container.
  - `auto` value means that the margins on the left and right of the container should be equal and they should be automatically calculated by the browser depending on the viewport.
  - As a result, the container will look centered inside of the body.

### CSS Theory 04: Types of Boxes

- ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/c847ce11-9184-4e07-8ff1-fcb72c426454)
- There are different types of boxes in CSS.
- Inline Boxes:
  - The types of boxes that only occupy exactly the space that they need for its content are called inline boxes.
- Block Boxes:
  - On the other hand, all other boxes, e.g. div, article, and paragraph are called block level boxes or block level elements.
  - They occupy all the space that they can and create line breaks after them. In other words, they cannot be side by side with one another.
- Block-Level Elements
  - Elements are formatted as blocks i.e. big blocks that occupy 100% of their parent element's width.
  - This is true even if the element doesn't require that much space.
  - They are stacked vertically by default, one after another.
  - The box model applies as showed earlier.
  - By default, most of the HTML elements are block-level elements.
  - These include: body, main, header, footer, section, nav, aside, div, h1-h6, p, ul, ol, li, etc.
  - One thing that we can do with CSS is to change from inline boxes to block level boxes, and we can do that with the `display` property set to the value of `block`.
- Inline Elements
  - Occupies only the space necessary for its content
  - Causes no line-breaks after or before the element
  - Box model applies in a different way: heights and widths do not apply
  - Paddings and margins are applied only horizontally (left and right)
  - These include: a, img, strong, em, button, etc.
  - You can change any element to an inline element by using the `display` property and setting its value to `inline`.
- This fundamental difference of how the box model works for inline elements is extremely important to always keep in mind.
- Inline-Block Element
  - Inline-block element is a mix of inline and block level.
  - They look like inline from the outside, behaves like block-level on the inside.
  - This means that they only occupy the space that need for the content and therefore, they do not cause any line-breaks.
  - But since they behave like block level elements on the inside - this means that the box model applies just as it does for block level elements i.e. we can set heights and widths and we can use margins and paddings just like on block level elements.
  - Essentially, inline block boxes really combine the best of both block and inline level elements.
  - In order to create an inline block element, all we have to do is to set the `display` property to `inline-block`, that's it.
- Chaining pseudo classes

> [!NOTE]
> Images are inline-block boxes.

### CSS Theory 05: Absolute Positioning

- Normal Flow vs. Absolute Positioning
  - Normal Flow
    - Default positioning (`position: relative`)
    - Element is "in flow"
    - Elements are simply laid out according to their order in the HTML code.
  - Absolute Positioning
    - Allows us to absolutely position an element across the page.
    - `position: absolute`
    - Element is removed from the normal flow: "out of flow"
    - The absolutely positioned element completely loses any impact on surrounding elements and in fact, it might even overlap them.
    - We use `top`, `bottom`, `left`, or `right` to offset the element from its **relatively positioned container**.
    - By default, the absolutely positioned element is positioned in relation to the view port, which is the visible part of the page.
    - However, that is usually not what we want.
    - We want to absolutely position the element in relation to some other parent element.
    - In order to do that, we need to specifically set the position of that parent element to relative.

> [!NOTE]
>
> To absolutely position an element with a relatively posiitoned parent element, the absolute element NEEDS to be a child of relative element. Otherwise it won't work.

- Summary
  - With absolute positioning you can basically put any element that you want wherever you want it to be on the page.
  - However, it is important that you do not abuse this newfound power i.e. don't use it build complex layouts, for example.
  - Instead, we use absolute positioning for single elements like a button.

### Pseudo-Elements

- Pseudo elements are elements that don't exist in the HTML but, we can still select and style them in CSS.
- Some examples:
  - First letter of a paragraph
  - First line of a paragraph
- Pseudo Elements:
  - `::first-letter`
  - `::first-line`
- Adjacent Element Selector or Adjacent Sibling Selector (`+`)
  - A sibling element is basically an element that is part of the same parent.
  - Adjacent Sibling is a sibling which is the very next element of the element selected.
  - Example:

```css
/* Only the paragraphs that are immediately after h3 are selected */
h3 + p::first-line {
  color: red;
}
```

> [!NOTE]
> Pseudo-classes are written with one colon e.g. `:hover`, and pseudo-elements are written with two colons e.g. `::first-letter`.

- After and Before Pseudo Elements (most used and most important pseudo elements)
  - They are often used to add cosmetic content to an element with the `content` property. It is inline by default.
  - `::after` - creates a pseudo-element that is the last child of the selected element.
  - `::before` - creates a pseudo-element that is the first child of the selected element.
  - This might sound strange but, it can be very useful for some small cosmetic style for which we don't necessarily want to add a new element to the HTML.
  - In `::before` and `::after` pseudo-elements, the `content` property is mandatory to mention, even if its value is just an empty string. Otherwise, it won't work.
  - By default, any pseudo-element is actually an inline element. So, if we want to give it any padding, we want the box model to apply to it normally. To do that we set the `display` property to `inline-block`.
- Setting negative values to `top`, `left`, `right`, and `bottom` in absolute positioning.

### Developer Skill 01: Googling and Reading Documentation

- [Stack Overflow](https://stackoverflow.com/)
- [MDN Docs](https://developer.mozilla.org/en-US/)
- [CSS Tricks](https://css-tricks.com/)
- [W3 Schools](https://www.w3schools.com/) (Not Recommended)

### Developer Skill 02: Debugging and Asking Questions

- [Markup Validation Service](https://validator.w3.org/)
- [Diff Checker](https://www.diffchecker.com/)
- A rule of thumb: Besides the rules that we already learned before about selector priority, if one selector is way more complex than the other, then many times, it is the more complex one that gets applied. Therefore, avoid writing complex selectors.

### Challenge 03

- CSS Properties:
  - `letter-spacing`

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
