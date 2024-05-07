# Section 04: Layouts: Floats, Flexbox, and CSS Grid Fundamentals

**About:** In this section, we will learn how to use CSS to build layouts using floats, flexbox, and CSS grid.

## Table of Content

- [Section 04: Layouts: Floats, Flexbox, and CSS Grid Fundamentals](#section-04-layouts-floats-flexbox-and-css-grid-fundamentals)
  - [Table of Content](#table-of-content)
  - [Lessons Learned](#lessons-learned)
    - [The 3 Ways of Building Layouts](#the-3-ways-of-building-layouts)
    - [Using Floats](#using-floats)
    - [Clearing Floats](#clearing-floats)
    - [Building a Simple Float Layout](#building-a-simple-float-layout)
    - [box-sizing: border-box](#box-sizing-border-box)
    - [Introduction to Flexbox](#introduction-to-flexbox)
    - [Flexbox Overview](#flexbox-overview)
  - [Author](#author)

## Lessons Learned

### The 3 Ways of Building Layouts

- What is Layout?
  - Layout is the way text, images, and other content is placed and arranged on a webpage.
  - Layout gives the page a visual structure, into which we place our content.
  - **Building a layout:** Arranging page elements into a visual structure, instead of simply having them placed one after another.
- Page Layout vs. Component Layout
  - Page layout is basically what we have been talking about up until this point, which is laying out the elements (the big pieces of content inside of a webpage/website).
  - On the other hand, these bigger page layouts are themselve made up of components.
  - These components themselves, need to have some kind of layout because they are made up of smaller pieces of content, which also need to be arranged in some kind of way.
- The 3 Ways of Building Layouts with CSS
  - Floats
    - The old way of building layouts of all sizes, using the `float` CSS property.
    - Still used but is getting outdated, fast.
  - Flexbox
    - Modern way of laying out elements in a 1-dimensional row without using floats.
    - Perfect for component layouts.
  - CSS Grid
    - For laying out element in a fully-fledged 2-dimensional grid.
    - Perfect for page layouts and complex components.

### Using Floats

- ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/5af210af-7e77-4c95-b9f6-b82af77ca74a)
- Float elements kind of behave like absolutely positioned elements.
- Floats are not actually a positioning scheme, like absolute positioning but, they are still another way in which elements can be out of flow.
- When an element is floated, it is removed out of the normal flow.
- What's different about this is that floating elements still have an impact on the surrounding elements.
  - Text and inline elements will actually wrap around the floated element.
- The container element will not adjust its height to the floated element. Therefore, it results in <ins>collapsing element</ins> phenomenon.
- CSS Properties:
  - `float`

### Clearing Floats

- Using the `clear` property on the last adjacent sibling of floated elements would fix the issue of collapsing elements.
- Another way to fix collapsing elements is "Clear fix hack".
  - On the element which has the collapsed height, we add a class called "clearfix".
  - In CSS, we select the "clearfix" class and add, in particular, the `::after` pseudo element.
    - Remember that `::after` pseudo element creates a new element which will be the last child element of the container.
    - Doing this is exactly the same as creating an empty div with the class of "clear" but, without having to clutter the HTML.
  - Now we can simply use the `clear` property on the pseudo element and set it to `both`.

> [!NOTE]
> Clearing floats only works on block level element.
>
> So, when using the clear fix hack, make sure to set `display` to `block`.
>
> Also, remember that `::after` won't show unless you use `content: ""` so, don't forget to mention that as well.

- CSS Properties:
  - `clear`

### Building a Simple Float Layout

- Using the `float` and `clear` property to create a simple layout using footer, aside, and article.

### box-sizing: border-box

- ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/55a0ef68-9936-4ce0-8cc4-480b41d234b3)
- `box-sizing: border-box`
- This tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to 100 pixels, that 100 pixels will include any border or padding you added, and the content box will shrink to absorb that extra width.
- This typically makes it much easier to size elements.

> [!NOTE]
> The default value (default behavior) of `box-sizing` is `content-box`.

> [!NOTE] > `box-sizing` is not one of those properties that get inherited. So, in order to apply it all the elements on a webpage/website, use it on the universal selector.

### Introduction to Flexbox

- Flexbox
  - Flex Container
  - Flex Items
- CSS Properties
  - `display: flex`
  - `align-items`
  - `justify-content`

### Flexbox Overview

- What is Flexbox?
  - It is a set of related **CSS properties** for **building 1-dimensional layouts**.
  - The main idea behind flexbox is that empty space inside a container element can be **automatically divided** by its child elements.
  - Flexbox makes it easy to automatically **align items to one another** inside a parent container, both horizontally and vertically.
  - Flexbox solves common problems such as **vertical centering** and creating **equal-height columns**.
  - Flexbox is perfect for **replacing floats**, allowing us to write fewer and cleaner HTML and CSS code.
- Flexbox Terminology
  - ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/ce020064-b964-401e-9baf-aacfeb105d9d)
  - The element on which we want to use Flexbox is called the **flex container**.
  - All we have to do in order to create a flex container is to set its `display` property to `flex`.
  - If we do this, then all the direct children of that flex container will become the so-called **flex items**.
  - This is important to know and to keep in mind because we will use different properties on the flex container and on the flex items.
  - The direction in which these flex items are laid out is called the **main axis**.
  - The other, perpendicular axis is simply called the cross axis.
  - It is important to know about these names because we can actually change the direction of the main axis, and therefore, also of the cross axis.
  - We can align elements along the main axis and along the cross axis in different ways.
  - Therefore, we always need to know which axis we are dealing with.
- Flex Properties
  - Flex Container
    - `gap`
    - `justify-content`
    - `align-items`
    - `flex-direction`
    - `flex-wrap`
    - `align-content`
  - Flex Items
    - `align-self`
    - `flex-grow`
    - `flex-shrink`
    - `flex-basis`
    - `flex`
    - `order`

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
