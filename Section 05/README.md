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

## Author

- [@bhoamikkhona](https://github.com/bhoamikkhona)
