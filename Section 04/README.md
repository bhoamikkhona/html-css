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
    - [Spacing and Aligning Flex Items](#spacing-and-aligning-flex-items)
    - [The Flex Property](#the-flex-property)
    - [Adding Flexbox to Our Project](#adding-flexbox-to-our-project)
    - [Building a Simple Flexbox Layout](#building-a-simple-flexbox-layout)
    - [Introduction to CSS Grid](#introduction-to-css-grid)
    - [A CSS Grid Overview](#a-css-grid-overview)
    - [Placing and Spanning Grid Items](#placing-and-spanning-grid-items)
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

### Spacing and Aligning Flex Items

- `justify-content` is used to align items along the main axis.
- `align-items` is used to align items along the cross axis.
- `order`:
  - The `order` property is designed to lay the items out in ordinal groups. This means that items are assigned an integer that represents their group. The items are then placed in the visual order according to that integer, lowest values first. If more than on item has the same integer value, then within that group the items are laid out as per source order.
  - As an exmaple, we have 5 flex items, and assign `order` values as follows:
    - Source item 1: `order: 2`
    - Source item 2: `order: 3`
    - Source item 3: `order: 1`
    - Source item 4: `order: 3`
    - Source item 5: `order: 1`
    - These items would be displayed on the page in the following order:
    - Source item 3: order: 1
    - Source item 5: order: 1
    - Source item 1: order: 2
    - Source item 2: order: 3
    - Source item 4: order: 3
    - ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/5570b6ff-6a00-408c-b057-6b634596bb15)
  - You can play around with the values and see how that changes the order.
  - Also, try changing `flex-direction` to `row-reverse` and see what happens -- the start line is switched so the ordering behings from the opposite side.
  - Flex items have a default `order` value of `0`, therefore items with an integer value greater that 0 will be displayed after any items that have not been given an explicity `order` value.
  - You can also use negative values with `order`, which can be quite useful.
  - If you want ot make one item display first and leave the order of all the other items unchanged, you can give that item order of `-1`. As this is lower than 0 the item will always be displayed first.
- `gap`

### The Flex Property

- `flex` property:
  - It is used to size flex items.
  - It is a short-hand for `flex-grow`, `flex-shrink`, and `flex-basis`.
- Default Values:
  - `flex-grow: 0`
  - `flex-shrink: 1`
  - `flex-basis: auto`
- `flex-basis`
  - When we want to size flex items and in particular with a width, then we usually do not use the `width` property but instead, we use `flex-basis`.
  - If we want our elements to have a width of 100px: `flex-basis: 100px`
  - Now, some of the items might have a width of 100px but, when the content is larger than 100px then the element actually extends to fit that content.
  - This means that `flex-basis` is not really rigid.
  - It is more like a recommendation that we make to the browser, but the browser will then, based on the content, figure out the optimal length.
  - If there is not enough space in the flex-container to fit the items witht he size that we describe in the `flex-basis`, then the flexbox is allowed to shrink the flex items by default because `flex-shrink` is set to 1 by default.
  - However, if we want to change that, we can simply set `flex-shrink` to `0`. But then as a result, the flex-items may overflow out of the flex container.
  - Therefore, setting `flex-shrink` to `0` is not advisable but, in some situations, it is necessary.
- `flex-shrink` - It determines whether the flexbox is allowed to shink flex items if necessary or not.
- `flex-grow`
  - Finally, there is also the opposite of that, which is `flex-grow` - which determines whether elements are allowed to grow as large as they can or not.
  - The `flex-grow` CSS property sets the flex grow factor, which specifies how much of the flex container's remaining space should be assigned to the flex items's main size.
  - When the flex-container's main size is larger than the combined main sizes of the flex items, the extra space is distributed among the flex items, with teach item growth being their growth factor value as a portion of the sum total of all the container's items' flex grow factors.
  - The `flex-grow` property is specified as a single number.
  - Negative values are invalid. Defaults to 0.
- `flex` shorthand:
  - `flex: flex-grow flex-shrink flex-basis`

> [!NOTE]
> Margins don't work in CSS Grid. Only `gap` would work.

### Adding Flexbox to Our Project

### Building a Simple Flexbox Layout

### Introduction to CSS Grid

- In CSS Grid, we have **grid container** and **grid items**.
- CSS Properties
  - `display: none`
  - `display: grid`
  - `grid-template-columns`
  - `grid-template-rows`
  - `gap`
  - `column-gap`
  - `row-gap`

### A CSS Grid Overview

- What is CSS Grid?
  - CSS Grid is a set of **CSS Properties** for **building 2-dimensional layouts**.
  - The main idea behind CSS Grid is that we **divide a container element into rows and columns** that can be filled with its child elements.
  - In two-dimensional contexts, CSS Grid allows us to write **less nested HTML** and **easier-to-read CSS**.
  - CSS Grid is **not meant to replace flexbox!** Instead, they work perfectly together. Need a **1D** layout? Use flexbox. Need a **2D** layout? Use CSS Grid.
- CSS Grid Terminology
  - ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/7425b4ef-cbe9-4355-afb5-420e03092d7e)
  - Grid Container:
    - This is where everything happens and we create a grid container by setting its `display` property to `grid`.
  - Grid Items:
    - All the child elements of the grid container will be the grid items.
  - Row Axis and Column Axis
    - Unlike flexbox, we cannot change the direction of the row and column axis - which makes it a bit easier ot work with CSS Grid.
  - ![image](https://github.com/bhoamikkhona/html-css/assets/143898153/fdf57915-36cc-4436-be2b-26c33b77d1bd)
    - Grid Lines:
      - Lines that basically divide up the grids and separate the columns adn the rows.
      - These grid lines are numbered from 1 to number of columns + 1 and 1 through number of rows + 1.
      - These numbers are important because we can use them to place a grid item exactly in one place in the grid where we want it to be.
      - The intersection of all these grid lines (grid lines for rows and columns) creates areas in which we can place our grid items.
      - These areas are called the grid cells.
    - Grid Cells
      - Grid cells are always created but, they don't always need to be filled.
    - Gaps/Gutters
      - As we saw in the last lesson, we can create spaces between the grid items. These are then called gutters or gaps.
      - For that we use the following properties: `gap`, `row-gap`, `column-gap`.
    - Grid Track
      - A grid track can be a row or also a column.
      - Each of these are grid tracks.
      - In the example (image above), we have 2 row tracks and 3 column tracks.
      - We call them tracks because these concepts are a bit more about the space itself and not about the grid items.
- Grid Properties
  - Grid Container
    - `grid-template-rows`
    - `grid-template-columns`
    - `row-gap`
    - `column-gap`
    - `justify-items`
    - `align-items`
    - `justify-content`
    - `align-content`
  - Grid Items
    - `grid-column`
    - `grid-row`
    - `justify-self`
    - `align-self`

### Placing and Spanning Grid Items

- `fr` unit (fr stands for fractions)
- `repeat()`
- Implicit and Explicit rows
  - Explicit rows are the ones that we explicitly define in the `grid-template-rows` property.
  - Implicit rows are the ones that is automatically created when the defined grid is filled up and more space was needed.
    - There is a way to style implicit rows but, that isn't in the scope of this course.

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
