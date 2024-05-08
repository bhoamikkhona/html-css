# Section 05: Web Design Rules and Framework

**About:** In this section, we turn our focus towards web design. We will learn a collection of design rules and guidelines that we can apply to different design "ingredients". We will learn things like typography, color, spacing, images, and more.

## Table of Content

- [Section 05: Web Design Rules and Framework](#section-05-web-design-rules-and-framework)
  - [Table of Content](#table-of-content)
  - [Lessons Learned](#lessons-learned)
    - [Project Overview](#project-overview)
    - [Overview of Web Design and Website Personalities](#overview-of-web-design-and-website-personalities)
    - [Web Design Rules 01: Typography](#web-design-rules-01-typography)
    - [Implementing Typography](#implementing-typography)
    - [Web Design Rules 02: Colors](#web-design-rules-02-colors)
    - [Implementing Colors](#implementing-colors)
    - [Web Design Rules 03: Images and Illustrations](#web-design-rules-03-images-and-illustrations)
    - [Web Design Rules 04: Icons](#web-design-rules-04-icons)
    - [Implementing Icons](#implementing-icons)
    - [Web Design Rules 05: Shadows](#web-design-rules-05-shadows)
    - [Implementing Shadows](#implementing-shadows)
    - [Web Design Rules 06: Border-radius](#web-design-rules-06-border-radius)
    - [Implementing Border-Radius](#implementing-border-radius)
    - [Web Design Rules 07: Whitespace](#web-design-rules-07-whitespace)
    - [Web Design Rules 08: Visual Hierarchy](#web-design-rules-08-visual-hierarchy)
    - [Implementing Whitespace and Visual Hierarchy](#implementing-whitespace-and-visual-hierarchy)
    - [Web Design Rules 09: User Experience (UX)](#web-design-rules-09-user-experience-ux)
  - [Author](#author)

## Lessons Learned

### Project Overview

- HTML Elements
  - `<blockquote>`
  - `<section>`
  - `<span>`

### Overview of Web Design and Website Personalities

- Web Design vs. Development
  - Web designers create the overall look and feel of a website
  - Web developers implement the design using HTML, CSS, and JavaScript.
- Why take design seriously?
  - Good Design
    - Creates an immediate and lasting good impression of the brand or product.
    - Makes the user trust the brand right away.
    - Increases the user's perceived value of the brand or product.
    - Gives users exactly what they were looking for when coming to the site, e.g. purchasing a product or finding information.
  - Bad Design
    - Makes users believe the brand doesn't really care about their product or service.
    - Makes the user insecure about trusting the brand.
    - Makes the brand or product seem "cheap".
    - Leaves users confused, and makes it hard for them to reach their goal.
- Web Design Ingredients
  - Typography
  - Colors
  - Images/Illustrations
  - Icons
  - Shadows
  - Border-radius
  - Whitespace
  - Visual hierarchy
  - User Experience
  - Components/Layout
- Website Personalities
  - Serious/Elegant
  - Minimalist/Simple
  - Plain/Neutral
  - Bold/Confident
  - Calm/Peaceful
  - Startup/Upbeat
  - Playful/Fun

### Web Design Rules 01: Typography

- Typography is the art and technique of arranging type to make written language legible, readable, and appealing when displayed.
- Serif vs. Sans Serif
- Sans Serif
  - Inter
  - Open Sans
  - Roboto
  - Montserrat
  - Work Sans
  - Lato
- Serif
  - Merriweather
  - Aleo
  - Playfair Display
  - Cormorant
  - Cardo
  - Lora
- ToolBox
  - Google Fonts
  - Font Squirrel
- Font Sizes and Weights
  - Do not use font weight below 400
- Reading Experience
  - Use less than 75 characters per line

### Implementing Typography

- ToolBox
  - [TypeScale](https://typescale.com/)
- SPACING SYSTEM (px)
  - 2 / 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 80 / 96 / 128
- FONT SIZE SYSTEM (px)
  - 10 / 12 / 14 / 16 / 18 / 20 / 24 / 30 / 36 / 44 / 52 / 62 / 74 / 86 / 98

### Web Design Rules 02: Colors

- Make the main color match your website's personality: colors convey meaning!
- Use a good color tone! Don't choose a random tone or CSS named colors.
- Establish a color system
  - You need at least 2 types of colors in your color palette: a main color and a grey color.
  - With more experience, you can add more colors: accent(secondary) colors
  - For diversity, create lighter and darker "versions" (tints and shades)
- When and How to use Colors
  - Use your main color to draw attention to most important elements on the page.
  - Use colors to add interesting accents or make entire components or sections stand out.
  - Use colors strategically in images and illustrations
- Relations between colors and typography
  - On dark colored backgrounds, try to use a tint of the background ("lighter version") for text.
  - Text should usually not be completely black. Lighten it up - if it looks heavy and un-inviting.
  - Don't make text too light! Use a tool to check contrast between text and background colors.
    - The contrast ratio needs to be at least 4.5:1 for normal text and 3:1 for large text (18px+)
- ToolBox
  - [Open Color](https://yeun.github.io/open-color/)
  - [Tailwind CSS Color](https://tailwindcss.com/docs/customizing-colors)
  - [Flat UI Colors](https://flatuicolors.com/)
  - [Tint and Shade Generator](https://maketintsandshades.com/)
  - [Paletton](https://paletton.com/#uid=1000u0kllllaFw0g0qFqFg0w0aF)
  - [Coolors](https://coolors.co/)

### Implementing Colors

### Web Design Rules 03: Images and Illustrations

- Use Good Images
  - Different types of images: product photos, storytelling photos, illustrations, patterns
  - Use images to support your website's message and story. So only use relevant images!
  - Prefer original images. If not possible, use original-looking stock images (not generic ones!)
- Use Images Well
  - Try to show real people to trigger user's emotions
  - If necessary, crop images to fit your message
  - Experiment combining photos, illustrations, and patterns
- Handling Text on Images
  - Method 01: Darken or Brighten image (completely or partially, using a gradient)
  - Method 02: Position text into neutral image area
  - Method 03: Put text in a box
- Some Technical Details
  - To account for high-res screens, make image dimensions 2x as big as their displayed size
    - Scale Factor: Actual pixels the screen contains/Pixels represented on screen
    - On high-res screens, scale facotr is 2x or even 3x, on "normal" screens it's just 1x (1 physical pixel = 1 design pixel)
  - Compress images for a lower size and better performance
  - When using multiple images side-by-side, make sure they have the exact same dimensions
- Toolbox
  - [Unsplash](https://unsplash.com/)
  - [Pexels](https://www.pexels.com/)
  - [Drawkit](https://www.drawkit.com/)
  - [unDraw](https://undraw.co/)
  - [Squoosh](https://squoosh.app/)

### Web Design Rules 04: Icons

- Use a good icon pack
- Use only one icon pack. Don't mix icons from different icon packs
- Use SVG icons or icon fonts. Don't use bitmap image formats (.jpg and .png)!
  - SVG imagtes and icon fonts are vector based
  - They can scale indefinitely!
- Adjust to website personality! Roundness, weight, and filled/outlined depend on typography
- Use icons to provide visual assistance to text
- Use icons for product feature blocks
- Use icons associated with actions, and label them (unless no space or icon is 100% clear)
- Use icons as bullet points
- Use Icons Well
  - To keep icons neutral, use same color as text. To draw more attention, use different color
  - Do not confuse your users: icons need to make sense and fit the text or action!
  - Don't make icons larget than what they were designed for. If needed, enclose them in a shape
- ToolBox
  - [Phosphor icons](https://phosphoricons.com/)
  - [ionicons](https://ionic.io/ionicons)
  - [icons8](https://icons8.com/)
  - [heroicons](https://heroicons.com/)

### Implementing Icons

- HTML Element:
  - `<svg>`
- CSS Properties:
  - `stroke`
  - `fill`

### Web Design Rules 05: Shadows

- Shadow creates depth (3D): the more shadow, the further away from the interface the element is
- Shadows can be used on boxes and text
- You don't have to use shadows! Only use them if it makes sense for the website personality.
- Use shadow in small doses: don't add shadows to every element.
- Go light on shadows, don't make them too dark
- Use Shadows in the Right Situation
  - Use small shadows for smaller elements that should stand out (to draw attention)
  - Use medium-sized shadows for larger areas that should stand out a bit more
  - Use large shadows for elements that should really float abvoe the interface
  - Experiment with changing shadows on mouse interaction (click and hover)
  - Bonus: Experiment with glows (colored shadows)

### Implementing Shadows

- HTML Elements
  - `<figure>` - standard for displaying cards
- Shadow on Elements:
  - `box-shadow: horizontal-offset-value vertical-offset-value shadow-blur-value shadow-scale-value shadow-color`
    - `horizontal-offset-value` basically describes how much to the right do you want to shift your shadow. When it is 0, it is equal on both sides.
    - `vertical-offset-value` basically describes how much to the bottom do you want to shift your shadow.
    - `shadow-blur-value` - The larger this value, the bigger the blur so, the shadow becomes bigger and lighter. Negative values are not allowed. If not specified, it will be set to 0 (meaning that the shadow's edge will be sharp)
    - `shadow-scale-value` is optional. The default value is 0 - which essentially means that the scale of the shadow will be the same size as the element. Positive value would cause the shadow to expand and negative values will cause the shadow to shrink. It is usually not even mentioned.
    - `shadow-color` - Usually for shadows, we use a small opacity values for colors e.g. rgba(0,0,0,0.1)
    - e.g. `box-shadow: 0 20px 30px 0 rgba(0, 0, 0, 0.1)`
- Shadow on Text
  - `text-shadow: horizontal-offset vertical-offset blur color`
    - This is similar to box shadow but, it does not have `shadow-scale-value`
    - e.g. `text-shadow: 0 5px 3px rgba(0, 0, 0, 0.2)`

> [!NOTE]
> Text shadow is also useful when putting text on images, so that text can stand out.

### Web Design Rules 06: Border-radius

- Use border-radius well
  - Use border-radius to increase the playfulness and fun of the design, to make it less serious
  - Typefaces have a certain roundness: make sure that border-radius matches that roundness
  - Use border-radius on buttons, images, around icons, stand-out sections, and other elements

### Implementing Border-Radius

- CSS Properties
  - `border-radius`
  - `border-bottom-left-radius`
  - `border-bottom-right-radius`
  - `border-top-right-radius`
  - `border-top-right-radius`

### Web Design Rules 07: Whitespace

- Why Whitespace?
  - The right amount of whitespace makes designs look clean, modern, and polished
  - Whitespace communicates how different pieces of information are related to one another
  - Whitespace implies invisible relationships between the elements of a layout
- Where to use whitespace?
  - Use tons of whitespace between sections
  - Use a lot of whitespace between groups of elements
  - Use whitespace between elements
  - Inside groups of elements, try to use whitespace instead of lines
- How much whitespace?
  - The law of proximity:
    - The more some elements (or groups of elements) belong together, the closer they should be.
  - Start with a lot of whitespace, maybe even too much! Then remove whitespace from there
    - Too much whitespace looks detached, too little looks too crammed
  - Match other design choices. If you have big text or big icons, you need more whitespace
  - Try a hard rule, such as using multiples of 16px for all spacing

### Web Design Rules 08: Visual Hierarchy

- What is visual hierarchy?
  - Visual hierarchy is about establishing which elements of a design are the most important ones.
  - It is about drawing attention to the most important elements.
  - It is also about defining a "path" for users, to guide them through the page.
  - We use a combination of position, size, colors, spacing, borders, and shadows to establish a meaningful visual hierarchy between elements/components.
- Visual hierarchy fundamentals:
  - Position important elements closer to the top of the page, where they get more attention.
  - Use images midefully, as they draw a lot of attention (large images get more attention)
  - Whitespace creates separation, so use whitespace strategically to emphasize elements
- Visual Hierarchy for text elements
  - For text elements, use font-size, font-weight, color, and whitespace to convey importance.
  - What text elements to emphasize?
    - Titles
    - Sub titles
    - links
    - buttons
    - data points
    - icons
  - We can also de-emphasize less important text e.g. labels or secondary/additional info.
- Visual Hierarchy between components
  - Emphasize an important component using background color, shadow, or border (or multiple)
  - Try emphasizing some component A over component B by de-emphasizing component B
  - What components to emphasize?
    - Testimonials
    - Call-to-acton sections
    - Highlight sections
    - Preview cards
    - Forms
    - Pricing tables
    - Important rows/columns in tables
    - etc

### Implementing Whitespace and Visual Hierarchy

### Web Design Rules 09: User Experience (UX)

- What is user experience?
  - "Design is not just what it looks like and feels like. Design is how it works" - Steve Jobs
  - User interface (UI) is the visual presentation of a product. It is how the graphical interface looks and feels like.
    - Layout
    - Personality
    - Typography
    - Colors
    - Icons
    - etc
  - User Experience (UX) is the overall experience the user has while interacting with the product
    - Does the app feel logical and well thought out?
    - Does the navigation work intuitively?
    - Are users reaching their goals?
- UI and UX Design
  - UI is graphical interface => UI Design is what makes an interface beautiful
  - UX is experience with interface => UX Design is what makes an interface useful and functional
  - UX Design cannot exist without UI Design
- UX Design Guiding Principle: Goals
  - A website or application exists for a reason: a user has a goal for visiting it, and business has a goal for creating it
- UX rules for usablity
  - Don't design complicated layouts. Don't reinvent the wheel. Use patterns that users know
  - Make your call-to-action the most prominent element, and make the text descriptive
  - Use blue text and underlined text only for links
  - Animations should have a purpose and be fast: between 200 and 500 ms
  - In forms, align labels and fields in a single vertical line, to make the form easier to scan
  - Offer users good feedback for all actions: form errors, form success, etc. [web apps]
  - Place action buttons where they will create an effect (law of locality) [web apps]
- UX Rules for Website Content
  - Use a descriptive, keyword-focused headline on your main page. Don't be vague or fancy!
  - Only include relevant information, efficiently! Cut out fluff and make the content 100% clear
  - Use simple words! Avoid technical jargon and "smart-sounding" words
  - Break up long text with sub-headings, images, block quotes, bullet points, etc.

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
