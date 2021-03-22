# Templating with Mustache:
Javascript templating is a fast and efficient technique to render client-side view templates with Javascript by using a JSON data source. The template is HTML markup, with added templating tags that will either insert variables or run programming logic.

The template engine replaces variables and instances declared in a template file with actual values at runtime, and convert the template into an HTML file sent to the client.

Mustache is a logic-less template syntax. It can be used for HTML, config files, source code — anything. It works by expanding tags in a template using values provided in a hash or object.

It is often referred to as “logic-less” because there are no if statements, else clauses, or for loops. Instead, there are only tags. mustache.js is an implementation of the mustache template system in JavaScript.

Also, mustache supports various languages, we don’t need a separate templating system on the server side. Example: Mustache.render(“Hello, {{name}}”, { name: “Qusai” }); => {{name}} is a placeholder

# Flexbox:
The main idea behind the flex layout is to give the container the ability to alter its items’ width/height (and order) to best fill the available space (mostly to accommodate to all kind of display devices and screen sizes). A flex container expands items to fill available free space or shrinks them to prevent overflow.

In flexbox layout, items are laid out following either the main axis or the cross axis:

main axis – The main axis of a flex container is the primary axis along which flex items are laid out.

main-start | main-end – The flex items are placed within the container starting from main-start and going to main-end.

main size – A flex item’s width or height, whichever is in the main dimension, is the item’s main size.

cross axis – The axis perpendicular to the main axis is called the cross axis. Its direction depends on the main axis direction.

cross-start | cross-end – Flex lines are filled with items and placed into the container starting on the cross-start side of the flex container and going toward the cross-end side.

cross size – The width or height of a flex item, whichever is in the cross dimension, is the item’s cross size.

Properties of flex container:
- display: creates a flex layout context.

- flex-direction.

- flex-wrap.

 - flex-flow:

- justify-content: defines how it is distributed the remaining 

- space.

- align-items.

- align-content.

Properties of flex items:

- flex-grow.
- flex-shrink.
- flex-basis.
- flex.
- align-self.
- align-items.
- align-content.