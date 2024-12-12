# Uncommon HTML Bug: Unexpected Null from getAttribute()

This repository demonstrates a subtle bug in HTML related to using the `getAttribute()` method.  The issue arises when attempting to retrieve an attribute that doesn't exist on an element.  Instead of throwing an error, `getAttribute()` silently returns `null`, which can lead to unexpected behavior in your JavaScript code if not properly handled.

## The Bug

The `bug.html` file contains a simple HTML structure with a div element.  The associated JavaScript code attempts to retrieve a non-existent attribute using `getAttribute()`.  This results in a `null` value being assigned to the variable `myVariable`, without any explicit error messages in the browser's console.

## The Solution

The `bugSolution.html` file provides a corrected approach. It includes a check for the existence of the attribute before attempting to retrieve its value, using hasAttribute(). This prevents unexpected null values and improves the robustness of the code.

## How to Reproduce

1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Open your browser's developer console (usually F12).  Observe the `null` value logged to the console.  No error is thrown.
4. Open `bugSolution.html` to see how the issue can be fixed.
