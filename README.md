# Inconsistent `calc()` Behavior in Media Queries

This repository demonstrates a bug related to the inconsistent behavior of the `calc()` function in CSS media queries when using a mix of percentage and pixel units.  Some browsers may not correctly evaluate the expression `calc(100vw - 100px)`, leading to unexpected rendering results.

## Bug Description
The `calc()` function, while powerful, exhibits inconsistencies when used within media queries, particularly when combining percentage units (like `vw`) with fixed-unit values (like `px`).  This can result in styles failing to apply correctly in certain browsers due to differing interpretations of the calculation.

## Reproduction
The `bug.css` file demonstrates the problematic code.  You can observe the inconsistent application of the styles across different browsers by resizing your viewport.

## Solution
The `bugSolution.css` file provides a workaround to mitigate this issue. This approach uses a more robust calculation that avoids the direct combination of percentage and pixel units inside the media query `calc()` function.