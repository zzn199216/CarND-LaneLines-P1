# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidYellowCurve2.jpg "solidYellowCurve2"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale use gray = grayscale(img)  ,then I use gaussian_blur() on grayscaled image . after, i use canny(to) hold the edge line in threshold,then use region_of_interest() to hold the edge in vertices rect area.after that,i use weighted_img to draw the line on the first image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by change the thickness to 15

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when some of the white area are not in connected .

Another shortcoming could be when there is a lot noise area, the pipeline just draw awful.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make area not just a rect area. but between 2 rect

Another potential improvement could be to make it not just gray. but recognise color . 
