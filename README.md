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

* **HTML**: We have a `div` element and an `input` element. The `div` will be styled dynamically, and the `input` will capture user input.
* **CSS**: The `div` is given a fixed height and width, a solid border, and a transition property to animate changes.
* **JS**: We select the `div` and `input` elements using `document.querySelector`. We add an event listener to the `input`
element that listens for `input` events. When the user types into the input field, the `border-radius` and `background` properties of the `div` are updated to match the input value.

### Example Inputs:
* Enter `red` to change the background color to red.

![image](https://github.com/user-attachments/assets/8c515f86-f972-4319-bf65-8789041a0bc9)

* Enter `50%` to change the `div` into a circle by setting the `border-radius` to 50%.

![image](https://github.com/user-attachments/assets/cff9f66e-857b-4f4f-90cb-136806548b85)
