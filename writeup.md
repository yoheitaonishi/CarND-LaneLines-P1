# **Finding Lane Lines on the Road** 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 
1. I converted the images to grayscale
2. I blur images
3. I apply images to canny transfer
4, masked images
5. I output images with hough lines

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline

* My pipeline can't detect curved lean lines
* My pipeline detect guardrail at challenge.mp4

### 3. Suggest possible improvements to your pipeline

* In order to detect curved lean lines, my pipeline should use  cv2.HoughLines() for detecting lean lines. ( http://docs.opencv.org/3.0-beta/doc/py_tutorials/py_imgproc/py_houghlines/py_houghlines.html )
* In order to detect curved lean lines, my pipeline should decide canny edge's thresholding automatically. ( http://www.kerrywong.com/2009/05/07/canny-edge-detection-auto-thresholding/ )
* In order not to detect guardrail, my pipeline should use new algorithm in this paper. ( http://airccj.org/CSCP/vol5/csit53211.pdf )
