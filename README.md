EXP NO 6: EDGE-DETECTION
Name:nithish kumar s
Register No: 212224230190
Date:28:04:2025
Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

Software Required:
Anaconda - Python 3.7

Algorithm:
Step1:
Import all the necessary modules for the program.

Step2:
Load a image using imread() from cv2 module.

Step3:
Convert the image to grayscale

Step4:
Using Sobel operator from cv2,detect the edges of the image.

Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

Program:
NAME:Vignesh.v REG NUMBER:212223230241

import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
image

SOBEL EDGE DETECTOR
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
image

LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
image

CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
image


<img width="691" height="539" alt="image" src="https://github.com/user-attachments/assets/c79fde56-7ff8-4a99-bdf9-b65c7b1b42b1" />


<img width="659" height="508" alt="image" src="https://github.com/user-attachments/assets/ef7f10eb-1ee7-4841-a409-52fee3d2812a" />
<img width="630" height="518" alt="image" src="https://github.com/user-attachments/assets/e19d05c2-b2d1-43d2-8aea-aff2b69000ee" />

<img width="655" height="501" alt="image" src="https://github.com/user-attachments/assets/f87de22f-6949-4a6e-adf4-8f098dc222b7" />



Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
