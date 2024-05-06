## Canny Edge Detection using Python
## i)Implementation of the Canny edge detection algorithm on a sample image to obtain the edges.
'''
## Developed By : K KESAVA SAI
## Register Number : 212223230105
## Code :
```PY
import cv2
import numpy as np
image = cv2.imread('cat.jpg', 0)  # Reading the image in grayscale mode
blurred = cv2.GaussianBlur(image, (5, 5), 0)  # 5x5 kernel size, sigma = 0
edges = cv2.Canny(blurred, 100, 200)
cv2.imshow('Original Image', image)
cv2.imshow('Canny Edges', edges)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## OUTPUT :
![image](https://github.com/Kesavasai20/CANNY-EDGE-DETECTION/assets/138849303/13032ccf-ba98-4686-a7cf-1e38c92f6719)
## ii)How do different parameter settings impact the result?
Different parameter settings significantly impact computational outcomes, such as those in machine learning and optimization. For instance, choices like learning rates and regularization strength directly affect model performance and convergence speed. Moreover, parameters influence system robustness to noise and resource usage, necessitating a balance between efficiency and accuracy. Additionally, they play a pivotal role in generalization, interpretability, and managing the bias-variance tradeoff, highlighting the importance of thorough experimentation and tuning for optimal results.

## Different parameter settings can significantly impact the result:
## Thresholds (low and high):
These thresholds determine which edges are considered strong, weak, or non-edges. Lower values lead to more edges being detected, while higher values filter out weaker edges. Adjusting these thresholds can impact the sensitivity of edge detection.

## Gaussian blur kernel size:
The size of the Gaussian blur kernel affects the amount of smoothing applied to the image. Larger kernels result in more smoothing, which can reduce noise but may also blur edges.

## Sigma (standard deviation) for Gaussian blur:
Sigma controls the spread of the Gaussian kernel. Higher values result in more smoothing, while lower values preserve finer details. However, too much smoothing can cause edges to be lost.
