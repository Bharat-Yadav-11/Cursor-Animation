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

## Purpose

The purpose of this code is to create a visually appealing cursor animation that follows the user's mouse movements on the webpage. This effect can enhance the user experience and add a touch of interactivity to the website's design.

## Additional Notes

- You can further customize the cursor elements by modifying the CSS styles defined in the "bharat.css" file.
- This code snippet can be integrated into various web projects to add a cursor animation effect without the need for external libraries or complex JavaScript.

Feel free to adapt and expand upon this code to suit your specific design and interactivity requirements.
