animated-dv-wheels
==================

Playing with HTML 5 to create an animated overlay to domestic violence "informational wheels", the first about gay/lesbian issues.

I create two HTML 5 canvases, one to display an image from a file and overlay another transparency image (drawn dynamically) on
top of it, and the second to "zoom in" a section of the wheel (a pie wedge or "slice") that is moused over. 

No external libraries are used, this is straight, simple Javascript with HTML 5. No shims for unsupported browsers.

I make a constructor function for the "slices" to define radian start/end points of each slice (could have also used polar coordinates
in degrees), and a "viewing" radian (and Cartesian x/y) from which to start capturing the image for a zoom. Then I stick the slices
in an array for handy processing.

An event listener listens to every mouse move and figures out when the mouse enters a new slice by examining the radian of the mouse
position. I also added a cool little transparent ray that follows the mouse from the center of the image. Just 'cause.

This is just a simple one-off to play with HTML 5, but if I have the time I will expand it to several wheels and organize the code into something
more expandable and organized, perhaps using Backbone/Marionette, and with responsive web capabilities.
