# CSS calc() Unexpected Behavior

This repository demonstrates an uncommon issue encountered when using the `calc()` function in CSS with a combination of percentage and pixel units.  The issue occurs when the parent element's dimensions aren't explicitly defined or rely on percentages.

## Bug Description
The `calc()` function in CSS allows you to perform calculations directly within your stylesheets. However, combining percentage and pixel units within `calc()` can lead to unexpected results if the parent element's width or height is not explicitly set or calculated reliably. This is mainly because the percentage calculation might depend on the parent element's dimension which itself might not be defined. 

## How to reproduce
1. Clone this repository.
2. Open `bug.html` in your browser.
3. Observe the unexpected behavior of the inner element.

## Solution
The solution is to ensure the parent element has a well-defined width (or height) so that the percentage calculation is made with a well-known value.  This can be done by setting explicit pixel dimensions, using percentage but on an element whose dimension is well defined, or using other layout techniques like flexbox or grid.