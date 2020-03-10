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

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

Other than improving the draw_lines function, I did not modify any of the other helper functions and simply called each one to build my pipeline.  I also used the tuning parameters from the quizes as a guage--which he helped a great deal.

My pipeline consisted of 7 steps: First, 
1) Applied grayscale to images
2) Applied Gaussian Blur
3) Applied Canny Edge Detection
4) Applied region of interest
5) Applied Hough Transform
6) Applied Weighted_img 
7) Draw lines


I modified the draw_lines() function by calculating slopes, separating left and right lanes by -/+ slope values.  Then I used Numpy's polyifit linear regression function to fit and plot the lines.
![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


Other than my lack of experience in scientific Python and Jupyter; curvy roads, inclimate weather, residential streets with no lane markings, undeveloped roads.  My draw_lines improvement is is surely lacking  


### 3. Suggest possible improvements to your pipeline


