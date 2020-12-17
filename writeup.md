# **Basic Computer Lane Finding** 
In fulfillment of the requirements of the Udacity Self-Driving Car Engineer Nanodegree Program
16-DEC-2020

**Goals**

* Create an image processing pipeline that detects road lanes 
* Discover challenges in lane-finding
* Discover image-preprocessing techniques
* Apply Canny Edge detection and Hough transforms
* Discover limitations and additional improvements 

[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### The Pipeline. As part of the description, explain how you modified the draw_lines() function.
Final:
find yellow and white
edge detection
mask out unneeded areas
create lines based on edges detected
reduce lines to two left and right lanes
superimpose (annotate) lanes on final image

initially efforts started with:
grayscale, 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

### limitations:
lanes exhibit jitter, and need to be smoothed out.
lanes that are near-horizontal are not drawn - going off the road
lanes that are near-vertical are not drawn: - lane drifiting 
daytime sunny weather only


### areas of improvement
use theta (angle of incidence of line to horizontal) instead of slope
tweaking parameters
including average of previous n-frames in calculating the lane line could help reduce lane jitter
collect metrics such as how many frames had 1 or zero lanes detected,
time to process each frame to understand pipeline performance,
use CNN techniques to identify the lanes
draw line as a continuous curve!

> Written with [StackEdit](https://stackedit.io/).