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

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
