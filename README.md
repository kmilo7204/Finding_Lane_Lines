# Finding Lane Lines
Considered as the starting point for a Self-Driving Engineer due to its low complexity, this project will show an approach to find the lane boundaries on a video taken from the roof of a vehicle in the highway.

In this repository an algorithm based on pure computer vision techniques is shown and explained in order to provide a great guide for the reader.

<p align="center">
<img src = "https://github.com/kmilo7204/Finding_Lane_Lines/blob/master/demo_gif/Video_GIF.gif" width="650" height="400">
</p>

## Tools
The tools used to find the lane lines in the images and the videos were:
 - Python
 - OpenCV

## Script
Access the [Jupyter Notebook](https://github.com/kmilo7204/Finding_Lane_Lines/blob/master/Finding_Lane_Lines.ipynb) of the project. In it, the approach is explained and the result for each step is shown in an image.

## Approach 
The approach used in this project consists in seven steps:

1. Convert the RGB input image into a Grayscale image. See cell `4`
2. Smooth the Grayscale image with a Gaussian Blur filter to the Grayscale image. See cell `5`
3. Apply the Canny edge detector to the smoothed image. See cell `6`
4. Select and extract a region of interest (ROI) from the image. See cell `7`
5. Apply the Hough transform to find the lines and its points within the ROI. See cell `8` 
6. Group the lines based on their slope to find one that represents all of them. See cell `9`
7. Combine the input RGB image and the ROI image which contains the lines to display the detections. See cell `10`

Finally, in order to process each frame of the video and obtain the final output, a function that blends all of steps explained above is created. See cell `11`
