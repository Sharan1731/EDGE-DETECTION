# Experiment-6
# EDGE-DETECTION
### Developed by: SHARAN G
### Register Number: 212223230203
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:

### Developed by: SHARAN G
### Register Number: 212223230203

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('hasna.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
<img width="639" height="418" alt="download" src="https://github.com/user-attachments/assets/74283576-bf5c-40b9-8f01-7f7df14e4c6b" />
<img width="639" height="418" alt="download" src="https://github.com/user-attachments/assets/b29522dc-434a-4f6b-aab5-ac089a796a56" />
<img width="639" height="418" alt="download" src="https://github.com/user-attachments/assets/6f840196-f7c4-478d-a996-288f273d3ee8" />
<img width="639" height="418" alt="download" src="https://github.com/user-attachments/assets/4e5b681d-7b7d-4e0d-8b07-8801b17b315b" />
<img width="639" height="418" alt="download" src="https://github.com/user-attachments/assets/4ce8e7ff-d77e-4fd0-8748-bfa4c0d60b0a" />




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
