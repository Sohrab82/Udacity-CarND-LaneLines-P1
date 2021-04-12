# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

# The pipeline

    Convert the image to gray
    Run canny filter to find the edges in the gray image
    Define a ROI and filter out the rest of the edged image
    Apply Hough filter to find the lines
    Extend those lines and find out where they intersect with the lower edge of the image
    Find the closest (extended) lines to the middle of the lower edge of the image and use them as left and right road lanes

# Potential shortcomings with the current pipeline

    Curvy roads
    Cracks or shades on the surface of the road that can be found as lane markings
    High dependecy on the tuning parameters

# Possible improvements

    Use previous frames to get a better estimation of lane markings locations
    Use a clothoid or high degree curve instead of a line to estimate the lane markings
