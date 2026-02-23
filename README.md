**Ans 1.

getElementById(): selects one element using the unique ID. It returns a single element
getElementsByClassName() : Finds all elements with a given class name. It returns a html collection.
querySelector(): returns the first child element that matches a specified CSS selector(s) of an element
querySelectorAll(): returns all child elements that matches a CSS selector(s)

**Ans 2.
Create the element: Using the document.createElement() we will make a new element like a div or p.

Add content and attributes: Then we will set text content using element.textContent, 
We can add attributes using element.setAttribute(name, value) or by directly accessing properties 
like element.className or element.id.

Find the parent: Will choose an existing element in the page where the new element should go.

Insert it into the DOM: Will place the new element inside the parent node using parentElement.appendChild(newElement).


**Ans 3.
Event bubbling: Event bubbling is when an event that happens on a specific element “bubbles up” through its parent 
elements in the DOM hierarchy. In other words, the event starts at the target element and then moves upward to its ancestors.

How it works:

a. If we click a button inside a div tag.

b. The click event first triggers on the button (the target).

c. Then it automatically propagates (bubbles) to the parent <div>, then to its parent, and so on up to the <body> or <html>.

d. Any event listeners on these ancestor elements for the same event will also run, unless propagation is stopped with event.stopPropagation().


**Ans 4.
Event delegation: Event delegation is a technique where you attach a single event listener to a parent element 
instead of adding listeners to each child element. The parent listens for events from its children and decides what 
to do based on which child triggered the event.

Why it is useful:

a. Less code: You don’t need separate listeners for every child element.

b. Dynamic elements: Works for elements that are added to the DOM later.

c. Better performance: Fewer event listeners means less memory and faster execution.


**Ans 5.

preventDefault(): Stops the browser’s default action for an event (like following a link or submitting a form). It
only affects the default behavior of the element. Clicking a link but not navigating to the URL.

stopPropagation(): Stops the event from bubbling or capturing up/down the DOM tree.
Only affects the flow of the event through parent/child elements.Clicking a button inside a div but
 preventing the div’s click handler from running.
