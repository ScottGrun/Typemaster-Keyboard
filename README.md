# Frontend Mentor - Typemaster pre-launch landing page solution

This is a solution to the [Typemaster pre-launch landing page challenge on Frontend Mentor](). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

-   [Frontend Mentor - Typemaster pre-launch landing page solution](#frontend-mentor---typemaster-pre-launch-landing-page-solution)
    -   [Table of contents](#table-of-contents)
    -   [Overview](#overview)
        -   [The challenge](#the-challenge)
        -   [Screenshot](#screenshot)
        -   [Links](#links)
    -   [My process](#my-process)
        -   [Built with](#built-with)
        -   [What I learned](#what-i-learned)
        -   [Continued development](#continued-development)
        -   [Useful resources](#useful-resources)
    -   [Author](#author)
    -   [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

-   Be able to get a sense of Typemaster's brand
-   Learn about the Typemaster's unique features
-   View the page on multiple different breakpoints

### Screenshot

![](./preview.jpg)

### Links

-   Solution URL: [Add solution URL here](https://your-solution-url.com)
-   Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

1. Review the designs and check to see if a grid and design system are provided. If not I will attempt to create my own CSS design system and determine the best grid options.

2. Once I have created the design system using CSS variables I will identify different sections of the page and create a stylesheet for each to help with project organization.

3. I will go through and create a mobile-only version of the website first and then make my way up the breakpoints untill all required breakpoints are covered.

4. Once the page is complete I will go through and check to see if any margins, padding, font sizes, or the copy is off / different from the designs.

5. After that I will make an accessibility sweep and make sure that that all images have alt text, font colors meet WCAG guidelines, and the appropriate aria labels are added, and that the page tab order makes sense.

6. Add in any micro animations that are part of the design.

### Built with

-   Mobile-first workflow
-   Semantic HTML5 markup
-   CSS Variables
-   CSS Grid
-   Flexbox

### What I learned

I took on this challenge in an attempt to hone my knowledge of semantic HTML and modern CSS practices. There numerous things I learned throughout this project and listed below are some I would like to highlight:

I learned how to use the `<picture>` tag to render images at different resolutions. Using this tag instead of the standard `<img>` can improve page load speed on different devices, for example, on mobile devices, it doesn't make sense to render an image that is meant to be displayed at a desktop's resolution as the network speed is usually slower.

```html
<picture class="landing-img-container" data-aos="fade-left" data-aos-duration="500">
	<source media="(min-width:1024px)" srcset="./assets/desktop/image-keyboard.jpg" />
	<source media="(min-width:768px)" srcset="./assets/tablet/image-keyboard.jpg" />
	<img class="landing-img" src="./assets/mobile/image-keyboard.jpg" alt="Typemaster keyboard image" />
	<img id="landing-square" class="square" src="./assets//shared/pattern-square.svg" />
</picture>
```

I learned how to use the `calc(...)` property to calculate values. I found this especially useful when I needed to overlay a div that had padding applied to img underneath it.

```css
#orange-overlay {
	border-radius: 20px;
	width: calc(100% - 30px);
	mix-blend-mode: multiply;
	background-color: var(--orange-1);
}
```

### Continued development

Moving forward I would like to improve the accessibility of the website, the design itself has a few accessibility issues such as the color of the body text not meeting WCAG guidelines. I would also like to learn how to leverage CSS Grid even more and become less reliant on flexbox.

### Useful resources

-   [Animate on Scroll Library](https://michalsnik.github.io/aos/) - I found this library that was exactly what I was looking for to easily integrate various animations into this project with little overhead.

## Acknowledgments

This design came from Frontend Mentor which is a great site for finding complete designs to hone frontend development skillsets.
