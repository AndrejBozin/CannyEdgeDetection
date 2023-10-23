# Canny Edge Detection

Canny Edge Detection, developed by John F. Canny in the late 80s, is a powerful algorithm designed for single-response edge detection and precise edge localization. This algorithm has been widely used in computer vision and image processing to detect edges in images. It is optimized to identify an edge only once and minimize the creation of false edges from image noise. Additionally, it aims to maintain a low probability of failing to detect real edges and falsely marking non-edges. Achieving good localization means ensuring that the center of the true edge is as close as possible to the detected edges.

## Algorithm Overview

Canny Edge Detection involves a sequence of five fundamental steps:

1. **Conversion to Grayscale Image**: The Canny Edge Detection algorithm operates on grayscale images. To outline edges and leverage grayscale intensity, it is customary to begin with the conversion of a color image to a grayscale image.

2. **Image Smoothing**: In this step, a two-dimensional Gaussian kernel is convolved with the image. This process reduces high-frequency noise and lays the foundation for improved localization and single-response edge detection.

3. **Calculating Image Gradient**: The algorithm commonly employs the Sobel operator to compute gradient components, gradient magnitude, and gradient direction. This information is crucial for edge detection.

4. **Non-Maximum Suppression**: The Sobel operator results in thick edges. To address this, non-maximum suppression is utilized. It thins the edges down to a single-pixel width, effectively reducing noise.

5. **Hysteresis-Based Thresholding**: This step utilizes double thresholding to further decrease noise and eliminate false edges.
