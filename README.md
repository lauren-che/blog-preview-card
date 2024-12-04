# Frontend Mentor - Blog Preview Card Solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![Screenshot Preview](/assets/images/screenshot.png)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/blog-preview-card-12ffBjfXxq)
- [Live Site URL](https://blogpreviewcardlc.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Flexbox & Variables

### What I learned

#### 1. **Linking to Fonts in Folder Structure**

One of the challenges I encountered was linking custom fonts from my local folder structure to the CSS file. I initially had trouble referencing the correct file paths, which led to fonts not loading as expected.

##### Issue:
- The fonts in my project were stored in a local folder, but the browser couldn't find the fonts because the path wasn't correctly specified in the CSS file.

##### Solution:
- I used the `@font-face` rule to link to the fonts in my local folder. The key was ensuring that the path to the font files was correct relative to the CSS file.

##### Code:
```css
/* Linking to fonts from a local folder using @font-face */
@font-face {
  font-family: 'Figtree'; /* Define the font family */
  src: url('../assets/fonts/Figtree-VariableFont_wght.ttf') format('woff2'),
    /* Modern browsers */
      url('../assets/fonts/Figtree-Italic-VariableFont_wght.ttf') format('woff'); /* Fallback for older browsers */
}

/* Applying the font to the body */
body {
  font-family: 'Figtree', sans-serif; /* Apply the custom font */
}
```
##### Key Takeaway:

- It's important to ensure the relative path to font files is correct. If your fonts are in a folder, you need to reference them relative to the location of your CSS file.

#### 2. **Remembering to Use Flexbox for the Avatar Section**

In one part of this project, I needed to ensure that the avatar image and the user's name appeared side by side on the same line, rather than stacked on top of each other. Initially, I was struggling to get the layout right, as the elements were stacking vertically instead of aligning horizontally.

##### Issue:
- The avatar image and the user's name were displaying in a column (stacked on top of each other), even though I wanted them to appear on the same line, centered within their container.

##### Solution:
- I remembered that **Flexbox** is perfect for situations like this. By using **Flexbox**, I was able to align the avatar image and the text (name) in a row and center them horizontally within their container.

##### Code:
```css
/* Flexbox container for the avatar section */
.avatar-container {
  display: flex;
  align-items: center;
  gap: 12px; /* Adds space between the image and the name */
}

/* Styling for the avatar image */
.avatar {
  width: 32px;
}

/* Styling for the avatar name */
h4 {
  font-size: 14px;
}
```

### Continued development

In future projects, I want to continue refining my skills with **hover** and **focus** states, as these are essential for creating engaging and interactive user interfaces. While I have used hover effects successfully in this project, I feel there’s still much more to learn, especially when it comes to creating smooth and nuanced transitions, adding subtle animations, and ensuring that focus states are accessible for all users.

### Useful resources

- [Web Fonts](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Web_fonts) - This resource helped me gain a clearer understanding of how to correctly link and apply custom fonts in both HTML and CSS. I found the step-by-step instructions particularly helpful for avoiding common pitfalls like incorrect paths or syntax errors. This pattern is something I’ll definitely apply in future projects to ensure fonts are consistently and correctly applied across my web pages.
- [Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) - This article was incredibly helpful in solidifying my understanding of Flexbox. It provided clear explanations of key concepts like flex containers, flex items, and how properties like `justify-content` and `align-items` work together to create responsive layouts. The visual examples were especially valuable in helping me see how the properties affect layout behavior in real-time. Thanks to this resource, I now feel much more confident using Flexbox for positioning elements, and I'll definitely be applying these techniques in future projects. I highly recommend this article to anyone who’s still getting the hang of Flexbox.

## Author

- Website - [Lauren Ché](https://lauren-che.github.io/)
- Frontend Mentor - [@lauren-che](https://www.frontendmentor.io/profile/lauren-che)