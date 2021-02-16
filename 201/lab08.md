# Layout
CSS allow the designer to control and change the layout of the webpage as long as he want. As you know that CSS treat evey part of the HTML page as it surrounded by a box , from here you have to imagine that every part of your web page included in it's own box , then you can to change the characteristics of that box as you want.For example, you can specify the position of each box(part) inside the window for instance you can make a paragraphs follow something called **Normal flow** in which they appear one
after the other, vertically down
the page. or even you can make their postions relative to each other (Relative Positioning)
or you can make some parts of the page content float in which the remaining content will be around it.
 #### Note that When you use relative, fixed, or absolute positioning, boxes can overlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page. to solve this problem use (z-index). . Its value is a number, and the higher the number the closer that element is to the front. For example, an element with a z-index of 10 will appear over the top of one with a z-index of 5.

 &nbsp;

# screen size
There is no doubt that the individual users differs from each other in terms of the devices they use to open your website , therfore the size of the page content thagt you already specified may be changed according to the size of window that the user used.
There are mainly two methods to solve this problem:

1-**Fixed width layout**: in which
designs do not
change size as the
user increases
or decreases
the size of their
browser window.
Measurements tend
to be given in pixels. But this methodmay end up with big gaps
around the edge of a page if the user screen is bigger than your's.

2-**Liquid layout** in which designs
stretch and contract
as the user increases
or decreases the
size of their browser
window. They tend to
use percentages.But this method has some disadvantages such as If the user has a wide
window, lines of text can
become very long, which
makes them harder to read.
