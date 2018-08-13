# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. 

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I use gaussian_blur() function to smooth the image, after that I use canny() function to detect the edges, then I use Hough transfrom to find the lane lines, finally I plot the lane line on the original figure. 

In order to draw a single line on the left and right lanes, I wrote a function called cluster_lines_for_lanes() to first find the slope of left and right lines, then extrapolate line segments to the full extent of the lane. 

If you'd like to include images to show how the pipeline works, just pass the input folder name, image name and output folder name to function lane_finding_algorithm().

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming is that we hardcoded the parameters of Region Of Interest (ROI). When ROI changes, the algorithm will fail.  


### 3. Suggest possible improvements to your pipeline

A possible improvement would be use more advanced computer vision techniques to dynamically find ROI. 
