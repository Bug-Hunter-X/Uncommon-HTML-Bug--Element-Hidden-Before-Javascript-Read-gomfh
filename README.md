# Uncommon HTML Bug: Element Hidden Before Javascript Read

This repository demonstrates an uncommon bug in HTML where an element is hidden using JavaScript before the browser's rendering engine has a chance to fully load and display it.

## Bug Description
The bug results in a blank screen because the `div` element with the id "myDiv" is hidden using JavaScript immediately after it's created. The Javascript engine works before the HTML is loaded into the browser engine. The `setTimeout` function is used to delay showing the element for 1 second. This allows the element to be loaded into the browser, but causes a visual delay.  This is not ideal in production and should be avoided.

## Solution
The solution involves restructuring the code to ensure the element is rendered before JavaScript modifies its visibility.  The corrected HTML loads the div correctly and applies the CSS without any delay.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in your web browser.
3. Observe the blank screen initially. After 1 second, the text will appear.