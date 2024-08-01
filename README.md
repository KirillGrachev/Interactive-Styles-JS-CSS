# Creating Interactive Styles with JavaScript and CSS

In this tutorial, we'll walk through a simple example of how to use JavaScript to dynamically update CSS properties based on user input. We'll create a square div element and an input field. When the user types into the input field, the div's background color and border-radius will change in real time. This example demonstrates how to make interactive and responsive web elements.

## Step 1: HTML Structure

First, let's create the basic HTML structure. We need a `div` element to represent our box and an `input` element to capture user input.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Styles</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div></div>
    <input type="text" placeholder="Enter a color or radius">
    <script src="script.js"></script>
</body>
</html>
```

## Step 2: CSS Styling

Next, we'll style the `div` element to give it a fixed size, border, and transition effect. This will ensure that changes to its properties are smoothly animated.

```
/* styles.css */
div {
    height: 200px;
    width: 200px;
    border: 1px solid #333;
    transition: all 0.4s ease;
}
```

## Step 3: JavaScript Functionality

Now, we need to write JavaScript to handle the user input and apply the corresponding styles to the `div` element. We'll add an event listener to the input field that listens for input events and updates the `div`'s `border-radius` and `background` properties based on the input value.

```
// script.js
let box = document.querySelector("div");
let input = document.querySelector("input");

input.addEventListener("input", () => {
    box.style.borderRadius = input.value;
    box.style.background = input.value;
});
```

## Explanation
