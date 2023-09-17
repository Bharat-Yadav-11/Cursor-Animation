# Cursor Animation README

This README explains the functionality of the HTML and JavaScript code provided, which creates a cursor animation effect that follows the user's mouse movement.

## HTML Structure

The HTML code defines the basic structure of the webpage:

- `<!DOCTYPE html>`: Declares the document type and version.
- `<html lang="en">`: Specifies the language of the document (English).
- `<head>`: Contains metadata and external resources links.
  - `<meta charset="UTF-8">`: Specifies the character encoding as UTF-8.
  - `<meta http-equiv="X-UA-Compatible" content="IE=edge">`: Ensures compatibility with Internet Explorer.
  - `<meta name="viewport" content="width=device-width, initial-scale=1.0">`: Sets the viewport for responsive design.
  - `<link rel="stylesheet" href="bharat.css">`: Links an external CSS file named "bharat.css."
  - `<title>Cursor Animation</title>`: Sets the webpage title displayed in the browser tab.
- `<body>`: Contains the content of the webpage.
  - `<div class="content">`: Wraps the main content of the webpage.
    - `<h1>Cursor Follow on MouseMove</h1>`: Displays a heading.
    - `<p>`: Displays a Lorem Ipsum text.
  - `<div class="cursor"></div>`: Defines the first cursor element for animation.
  - `<div class="cursor2"></div>`: Defines the second cursor element for animation.

## Cursor Animation JavaScript

```javascript
var cursor = document.querySelector(".cursor");
var cursor2 = document.querySelector(".cursor2");
document.addEventListener("mousemove", function(e){
   cursor.style.cssText = cursor2.style.cssText = "left: " + e.clientX + "px; top: " + e.clientY + "px;";
});
```

- This JavaScript code adds interactive cursor animations to the webpage.
- It selects the cursor elements with the classes "cursor" and "cursor2" using `document.querySelector()`.
- The `document.addEventListener("mousemove", function(e) {...}` listens for the "mousemove" event on the document.
- When the user moves their mouse, it updates the CSS `left` and `top` properties of both cursor elements to match the current mouse coordinates (`e.clientX` and `e.clientY`).
- As a result, the cursor elements follow the mouse movements, creating a dynamic visual effect.

# CSS Code README

This README explains the purpose and structure of the provided CSS code, which is used to style and create cursor animation effects on a webpage.

## CSS Styles for Body

```css
body {
  margin: 0;
  padding: 0;
  background-size: cover;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-family: "Open Sans", sans-serif;
  color: #000;
  cursor: arrow;
}
```

- `body`: This selector defines styles for the entire webpage's body.
  - `margin: 0; padding: 0;`: Sets margin and padding to zero, removing any default spacing.
  - `background-size: cover;`: Ensures that the background image covers the entire viewport.
  - `height: 100vh;`: Sets the height of the body to 100% of the viewport height.
  - `display: flex;`: Uses a flexbox display to center content both vertically and horizontally.
  - `align-items: center;`: Vertically centers content.
  - `justify-content: center;`: Horizontally centers content.
  - `text-align: center;`: Centers text within its container.
  - `font-family: "Open Sans", sans-serif;`: Specifies the font family for text.
  - `color: #000;`: Sets the text color to black.
  - `cursor: arrow;`: Sets the default cursor style to an arrow.

## CSS Styles for Content Paragraph

```css
.content p {
  width: 700px;
  line-height: 26px;
  font-size: 18px;
  text-align: justify;
}
```

- `.content p`: This selector defines styles for paragraphs within an element with the class "content."
  - `width: 700px;`: Sets a maximum width for paragraphs to control line length.
  - `line-height: 26px;`: Defines the line height for better readability.
  - `font-size: 18px;`: Specifies the font size.
  - `text-align: justify;`: Justifies text within paragraphs.

## CSS Styles for Cursor Elements

```css
.cursor {
  position: fixed;
  width: 50px;
  height: 50px;
  border: 2px solid #000;
  border-radius: 50%;
  left: 0;
  top: 0;
  pointer-events: none;
  transform: translate(-50%, -50%);
  transition: .5s;
}

.cursor2 {
  position: fixed;
  width: 8px;
  height: 8px;
  background-color: #000;
  border-radius: 50%;
  left: 0;
  top: 0;
  pointer-events: none;
  transform: translate(-50%, -50%);
}
```

- `.cursor` and `.cursor2`: These selectors define styles for two cursor elements.
  - `.cursor`: Styles for the primary cursor element.
  - `.cursor2`: Styles for the secondary cursor element.
  - `position: fixed;`: Fixes the cursor elements in place on the viewport.
  - `width` and `height`: Define the dimensions of the cursor elements.
  - `border`: Adds a border to the primary cursor.
  - `border-radius: 50%;`: Rounds the cursor into a circle.
  - `left` and `top`: Initialize the cursor elements at the top-left corner.
  - `pointer-events: none;`: Ensures that the cursor elements don't interact with user clicks.
  - `transform: translate(-50%, -50%);`: Centers the cursor elements at the mouse pointer.
  - `transition: .5s;`: Applies a smooth transition effect with a duration of 0.5 seconds.

## Cursor Animation

```css
.content:hover ~ .cursor {
  transform: translate(-50%, -50%) scale(1.5);
  background-color: #c6c6c6;
  opacity: .5;
}

.content:hover ~ .cursor2 {
  opacity: 0;
}
```

- These rules define the behavior of cursor elements on hover over an element with the class "content."
- `.content:hover ~ .cursor`: When hovering over the content element, the primary cursor scales up, changes background color, and becomes semi-transparent.
- `.content:hover ~ .cursor2`: The secondary cursor becomes invisible (opacity set to 0) on content hover.


## Purpose

The purpose of this code is to create a visually appealing cursor animation that follows the user's mouse movements on the webpage. This effect can enhance the user experience and add a touch of interactivity to the website's design.

## Additional Notes

- You can further customize the cursor elements by modifying the CSS styles defined in the "bharat.css" file.
- This code snippet can be integrated into various web projects to add a cursor animation effect without the need for external libraries or complex JavaScript.

Feel free to adapt and expand upon this code to suit your specific design and interactivity requirements.
