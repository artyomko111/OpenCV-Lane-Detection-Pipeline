# 🚀 OpenCV Lane Detection Pipeline

## 📝 Project Summary

This repository contains an implementation of a classic lane line detection pipeline using computer vision techniques with Python and OpenCV. This method is a crucial component of Advanced Driver Assistance Systems (ADAS) and autonomous vehicles. The project aims to accurately identify and track lane lines on the road to enhance driving safety and convenience.

## ⚙️ Methodology (Pipeline Steps)

The lane detection is achieved through a sequential image processing pipeline:

    Color/HSV Thresholding: The input video frames (BGR format) are converted to the HSV (Hue, Saturation, Value) color space, which is better suited for color detection. Thresholding is then applied to detect the road's color and convert the image into a binary image, separating the road from the surrounding environment.

Gaussian Blur: Applied as a pre-processing step to reduce image noise and remove superfluous edges, keeping only the most salient edges for detection.

Canny Edge Detection: Used to extract all prominent edges in the image.

Region of Interest (ROI) Selection: A fixed polygonal area is defined to mask out uninteresting regions and focus solely on the lane lines, which significantly improves detection efficiency and speed.

Hough Transform: This method is used to extract straight lines from the detected edges within the ROI.

Line Averaging and Extrapolation: The multiple lines detected by the Hough Transform are averaged to derive a single, smooth lane line for both the left (negative slope) and right (positive slope) lanes. The lines are then extrapolated to form the complete lane lines.

## 🛠️ Technologies Used

    Python

    OpenCV (Computer Vision Library) 

    NumPy (for array operations/image masking)
