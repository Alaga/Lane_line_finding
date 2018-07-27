# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals of this project are the following:
* Make a pipeline that finds lane lines on the road
* Execute the pipeline in the videos, we should see one left and one right lane line.

---

### Pipeline

### 1. Gray scaling the image

* Gray scaling the image, helps us to the narrow the color component to single dimentional.
* This is useful in edge detection.

### 2. Blur the image

* Blurring the image, removes the noise from the image. Adds advantage in further processing.

### 3. Cranny edge detection

* This cranny edge detector API in openCV, transforms the image into edge highlighted image.

### 4. Region of interest

* Mask the portion of image, not into our interest.

### 5. Hough lines

* Hough transform will help us find the lines in the region of interest.

### 6. Left and right lanes

* Further, seperating the left and right lanes depending on the slope.
* plus, identifying the line points are in left or right half of the image.

### 7. drawing the lines over the lane mark

* Finding the average slope and intercepts of the left and right lanes, using numpy ployfit API.
* using the slope and intercepts, we draw the lanes in the region of interest.

Point 5, 6 & 7, are covered inside the hough_lines API in the helper.


---

### Improvement

* This pipeline doesn't work in all conditions of images. It fails in the challenge video.
* Need to work on converting into HSV or HSL component, and filter yellow & white lines.
* Need to fine tune the kernel_size, thresholds, hough parameter to draw smooth lane lines.
