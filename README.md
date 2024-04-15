# -Canny-Edge-Detection
# i)Implementation of the Canny edge detection algorithm on a sample image to obtain the edges.
# Developed By : Arikatla Hari Veera Prasad
# Register Number : 212223240014
# Code :
```
import cv2
import numpy as np

# Read the image
image = cv2.imread('username.jpg', 0)  # Read the image in grayscale

# Apply Gaussian blur to the image
blurred = cv2.GaussianBlur(image, (5, 5), 0)

# Apply Canny edge detection
edges = cv2.Canny(blurred, 100, 200)  # You can adjust the threshold values (100 and 200) as needed

# Show the original and detected edges
cv2.imshow('Original Image', image)
cv2.imshow('Detected Edges', edges)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
# OUTPUT :
![Screenshot 2024-04-15 173412](https://github.com/Hariveeraprasad-2006/-Canny-Edge-Detection/assets/145049988/783857b8-3481-4648-803f-5bd9ef3c0346)
![Screenshot 2024-04-15 173357](https://github.com/Hariveeraprasad-2006/-Canny-Edge-Detection/assets/145049988/9891a9a9-ecde-44bf-ad58-e0ef167cc027)
# ii)How do different parameter settings impact the result?
Different parameter settings in the Canny edge detection algorithm can have a significant impact on the resulting edge detection. The two main parameters to adjust are the low and high threshold values. Here's how different parameter settings can impact the result:

Low Threshold Value:

A lower low threshold value will result in more weak edges being detected in the image. This can include edges with lower gradient values, which may correspond to less prominent features in the image.
Increasing the low threshold value will reduce the number of weak edges detected, potentially eliminating noise or small features from the edge map.
High Threshold Value:

A lower high threshold value will result in more continuous edges being detected, including weaker edges and potentially noise. This can lead to a more complete edge map but may also introduce false positives.
Increasing the high threshold value will only detect stronger edges in the image, potentially filtering out weaker edges and noise. This can result in a cleaner edge map but may miss some edges, especially those with lower contrast.
Gaussian Blur Kernel Size:

The size of the Gaussian blur kernel used before edge detection affects the smoothness of the image and, consequently, the edge detection results. A larger kernel size will result in more smoothing and potentially blur out smaller details, affecting edge localization.
Conversely, a smaller kernel size will result in less smoothing and preserve finer details in the image, potentially leading to sharper edges in the edge map.
Image Gradient Calculation Method:

The choice of gradient calculation method (e.g., Sobel, Scharr) can impact the sensitivity of edge detection to noise and the sharpness of detected edges. Different methods may produce slightly different edge maps, especially in regions with high noise or texture.
