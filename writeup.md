# **Finding Lane Lines on the Road** 

## Writeup

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied the Gaussian filter.  Next, I applied Canny edge detection.  Lastly, I chose a region of interest and created Hough lines.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by calculating the slope and intercepts for a line on the right and left side of the road, then using those values to create new starting and ending points of the line.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there are tight turns on the road, so the lines are not very straight. 

Another shortcoming could be the algorithm not working at night.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make the pipeline more robust in its handling of the line creation.

Another potential improvement could be to identify lines outside of the region of interest.  For example, other lane lines to the right and left.
