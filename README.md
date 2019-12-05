# JavaScript30 #5: Flex Panels Image Gallery

Clicking a panel will toggle it between open and closed.

When closed, all five panels are narrow. When open, a panel grows wider and previously-hidden text moves into view from above and below (using CSS transitions).


## Future Iterations

Looking into a way to use arrow functions for the toggling. Issues I have to work around:

1. The `this` keyword will no longer work.
2. Switching `this` to `e.target` works *partially*, but creates other issues:
  - `e.target` changes depending exactly where the user clicks. They may click on the main panel container, or they may click on one of the three `<p>` tags inside the container. Whatever they click on is what gets toggled, and if it's not the main container, it doesn't work.
  - After the main container has been clicked, all three `<p>` tags are overlaying it and there is nowhere the user can click to toggle it closed again.
3. Everything I'm researching online is telling me not to use arrow functions for what I'm trying to accomplish.