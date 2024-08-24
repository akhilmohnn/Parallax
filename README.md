
## Overview
This README provides instructions for styling and structuring two sections of a webpage, `section1` and `section2`, using the provided CSS code.

## Instructions

1. **HTML and Body Setup:**
   - Set up the HTML and body to manage overflow and perspective.

2. **Section Styles:**
   - Style `section1` and `section2` to fill the viewport height and handle background images and text.

3. **Image Handling:**
   - Use `base.png` and `base-removed.png` as background images for `section1`.

4. **Text Transformations:**
   - Apply transformations to the text in both sections.

## Example CSS

```css
/* HTML and Body Setup */
html {
    height: 100vh;
    overflow: hidden;
}

body {
    width: 100vw;
    height: 100vh;
    margin: 0;
    background: #222;
    perspective: 1px;
    transform-style: preserve-3d;
    overflow-x: hidden;
    overflow-y: scroll;
}

/* Section Styles */
.section1, .section2 {
    width: 100%;
    height: 100vh;
    position: relative;
    transform-style: preserve-3d;
}

.section1::before {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    background: url("base.png") top center;
    background-size: cover;
    transform: translateZ(-1px) scale(2.2);
    filter: blur(2px);
}

.section1::after {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    background: url("base-removed.png") top center;
    background-size: cover;
}

.section1 .text {
    color: black;
    top: 10%;
    transform: translateZ(-0.5px) scale(1.5, 1.6) translate(-33%, 10%);
}

.section2 {
    background: rgb(68, 35, 19);
}

/* Text Styles */
.text {
    top: 30%;
    left: 50%;
    position: absolute;
    font-family: 'Franklin Gothic Heavy';
    font-size: 15vw;
    color: white;
    text-shadow: 2px 3px 5px rgba(0, 0, 0, 0.3), 5px 5px 70px rgba(255, 255, 255, 0.5);
    transform: scale(1, 1.1) translate(-50%, 10%);
}
```

## Notes
- Make sure to replace `"base.png"` and `"base-removed.png"` with the actual image paths.
- Adjust the `transform` properties as needed based on your design requirements.

