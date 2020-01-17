### Dropdown navigation background

As the user hovers over the nav links, the dropdown menu is displayed for each of them. The white background adjusts itself to the width and height of the individual dropdown, along with a nice transition.

We add event listeners on list items for mouseenter and mouseleave. We then make functions that handle enter and leave. 

The dropdown content is initially hidden both with opacity 0 and display none. Then on mouseenter it gets a class of trigger-enter that gives it a display block. After 150 milisecons it also gets a class of trigger-enter-active that sets opacity to 1, for a nicer appearance effect.

When dropdown gets both of those classes, it also gets the class open that adds white background.

Function handleLeave removes all of those classes.

To figure out the width, height, top and left positions, we call getBoundingClientRect on both dropdown and nav.

From there we make our own coords object and take the width and height from dropdown, but for the top and left we deduct top and left offset for nav, so that everything still works in case our html changes.
