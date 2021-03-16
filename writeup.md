# **Finding Lane Lines on the Road** 

### Reflection

### 1. The pipeline

- Convert the image to gray
- Run canny filter to find the edges in the gray image
- Define a ROI and filter out the rest of the edged image
- Apply Hough filter to find the lines
- Extend those lines and find out where they intersect with the lower edge of the image
- Find the closest (extended) lines to the middle of the lower edge of the image and use them as left and right road lanes

### 2. Identify potential shortcomings with your current pipeline

- Curvy roads
- Cracks or shades on the surface of the road that can be found as lane markings
- High dependecy on the tuning parameters

### 3. Suggest possible improvements to your pipeline

- Use previous frames to get a better estimation of lane markings locations
- Use a clothoid or high degree curve instead of a line to estimate the lane markings