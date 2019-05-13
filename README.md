# Finding Lane Lines
Considered as the starting point for a Self-Driving Engineer due to its low complexity, this project will show an approach to find the lane boundaries on a video taken from the roof of a vehicle in the highway.

In this repository an algorithm based on pure computer vision techniques is shown and explained in order to provide a great guide for the reader.

## Tools
The tools used to find the lane lines in the images and the videos were:
 - Python
 - OpenCV

## Approach 
The approach used in this project consists in seven steps:

1. Convert the RGB input image into a Grayscale image.
2. Smooth the Grayscale image with a Gaussian Blur filter to the Grayscale image.
3. Apply the Canny edge detector to the smoothed image.
4. Select and extract a region of interest (ROI) from the image.
5. Apply the Hough transform to find the lines and its points within the ROI. 
6. Group the lines based on their slope to find one that represents all of them.
7. Combine the input RGB image and the ROI image which contains the lines.

## Script
The [Jupyter Notebook](https://github.com/kmilo7204/Finding_Lane_Lines/blob/master/Finding_Lane_Lines.ipynb) presented in this project contains the algorithm to find the lane lines. The apporach explained before was implemented and the result of each step can be found within the script. 
