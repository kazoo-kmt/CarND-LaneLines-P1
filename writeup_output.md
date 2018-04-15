# **Finding Lane Lines on the Road** 



[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied gaussian blur. Then, I applied Canny edge detection to get the feature of the lane lines. After that, I cut off the image by specifying the region of interest. Finally, I applied Hough transformation to the detected features to get the line parameters. When I draw the lines on the image, I separated the lines from Hough transform based on its slope, then applied polynominal fitting to get a single line for both left and right lane. 

### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when using a differenet camera, this algorithm may not work because it's tuned to this specific camera's view when getting the region of interest.

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to incorporate camera parameters such as intrinsics and extrinsics. 
