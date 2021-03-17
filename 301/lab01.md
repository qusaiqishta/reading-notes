#  <span style="color:yellow"> RESPONSIVE WEB DESIGN and FLOATS</span>.


Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop. Responsive web design is focused around providing an intuitive and gratifying experience for everyone. Desktop computer and cell phone users alike all benefit from responsive websites.

&nbsp;

# <span style="color:yellow">Responsive vs Adaptive vs Mobile Designs: What’s the Difference?
</span>.

Responsive and adaptive web design are closely related, and often transposed as one in the same.
 
 - Responsive generally means to react quickly and positively to any change.

 - Adaptive means to be easily modified for a new purpose or situation, such as change.


 With responsive design websites continually and fluidly change based on different factors, such as viewport width, while adaptive websites are built to a group of preset factors. A combination of the two is ideal, providing the perfect formula for functional websites. Which term is used specifically doesn’t make a huge difference.

 - Mobile generally means to build a separate website commonly on a new domain solely for mobile users.

 [Responsive Web design](https://miro.medium.com/max/1250/1*qF8LfAwUhl57g9T0BVvVdg.jpeg)

 &nbsp;

 ## <span style="color:yellow">Flexible layouts
</span>.

Responsive web design is broken down into three main components, including flexible layouts, media queries, and flexible media.

- Flexible layouts, is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width.

- Media queries were built as an extension to media types commonly found when targeting and including styles. Media queries provide the ability to specify different styles for individual browser and device circumstances, the width of the viewport or device orientation for example.


*It is best not to use fixed measurement units such as pixels or inches because the viewport height and width are onstantly changing from device to device. The formula for aleviating this constraint is the following:*

target ÷ context = result

*This is taking the target width of the element, divide it by the width of its parent element. The result is the relative width of the target element.*

&nbsp;


 ## <span style="color:yellow">Flexible Media
</span>.
As viewports begin to change size media doesn’t always follow suit. Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

&nbsp;


 # <span style="color:yellow">Floats: What are they and what are they used for?
</span>.

Float is a CSS positioning property. In web design, page elements with the CSS float property applied to them are just like the print images in a magazine where the text flows around them. Settinf the float property of a css happens like this:

.image { float: right; }

This sets the image to the right side of the page with the content wrapped around it to the left side.

&nbsp;


 ## <span style="color:yellow">Four values for floating:

</span>.

1.Float: right; // floats elements to the right.

2.Float: left; // floats elements to the left

3.Float: none; // ensures the element willnot float. This is a default.

4.Float: inherent // assumes the float value from the elements parent element.

Floats can be used to create webpage layouts.