# Uncommon HTML Bug: Empty innerHTML After textContent

This repository demonstrates an uncommon bug in HTML related to manipulating the content of a div element using both `textContent` and `innerHTML`.  The issue arises when attempting to first set the `textContent` and subsequently setting `innerHTML` to an empty string.  This results in unexpected behavior where the div content is emptied, despite the `textContent` assignment.

## Bug Description:

The primary issue is the unexpected clearing of the div's content even when textContent has already been assigned. This is counterintuitive; one would expect the div to retain the content set by `textContent`.

## How to Reproduce:

1. Clone this repository.
2. Open the `bug.html` file in a web browser.
3. Inspect the `myDiv` element in your browser's developer tools.

## Solution:

The solution involves avoiding the use of `innerHTML` to empty the div after setting `textContent`.  Instead, the `textContent` should be directly set to an empty string. See `bugSolution.html` for corrected code.