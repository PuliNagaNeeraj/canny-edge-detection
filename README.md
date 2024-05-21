# canny-edge-detection
Implementation of the Canny edge detection algorithm on a sample image to obtain the edges.

### Developed By : PULI NAGA NEERAJ
### Register Number : 212223240130

## Code :
```
import cv2
import numpy as np
image = cv2.imread('flower.jpg', 0)  # Reading the image in grayscale mode
blurred = cv2.GaussianBlur(image, (5, 5), 0)  # 5x5 kernel size, sigma = 0
edges = cv2.Canny(blurred, 100, 200)
cv2.imshow('Original Image', image)
cv2.imshow('Canny Edges', edges)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output
![image](https://github.com/PuliNagaNeeraj/canny-edge-detection/assets/138849173/52596905-198f-4977-ae26-f37eb76d9c6e)

![image](https://github.com/PuliNagaNeeraj/canny-edge-detection/assets/138849173/74de0f37-36d6-48f1-8dad-5ad50a3535a6)

## How do different parameter settings impact the result?
### Different parameter settings in the Canny edge detection algorithm can significantly influence the detected edges:
## 1.Thresholds (low and high):
Changing the low and high thresholds affects which edges are classified as strong, weak, or non-edges. Lower thresholds may result in more edges being detected, potentially including noise, while higher thresholds filter out weaker edges. Adjusting these thresholds can thus impact the sensitivity of edge detection.

## 2 Gaussian blur kernel size:
The size of the Gaussian blur kernel determines the extent of image smoothing before edge detection. Larger kernel sizes lead to more smoothing, which can help reduce noise but may also blur edges, affecting their sharpness and clarity.

## 3.Sigma (standard deviation) for Gaussian blur:
Sigma controls the spread of the Gaussian blur kernel. Higher sigma values result in more aggressive smoothing, potentially leading to loss of fine details, including edges. Lower sigma values preserve finer details but may not effectively reduce noise.
