# Uncommon HTML Bug: Race Condition in DOM Manipulation

This repository demonstrates a subtle race condition that can occur in HTML when JavaScript attempts to manipulate the DOM (Document Object Model) before the browser has fully parsed and rendered the HTML.

## Bug Description
The script attempts to change the `innerHTML` of a `div` element before the browser has finished parsing the HTML. This can lead to the script failing silently or producing unexpected results, depending on the browser and its rendering engine. 

## How to Reproduce
Clone this repo and open `bug.html` in a web browser. You might see unexpected behavior or an error in the console. 

## Solution
The solution uses the `DOMContentLoaded` event listener which ensures that the JavaScript code executes only after the HTML is fully parsed.  See `bugSolution.html` for a fix.