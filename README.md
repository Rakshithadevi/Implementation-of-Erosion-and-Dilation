# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages.

## Step2:
Create the Text using cv2.putText.

## Step3:
Create the structuring element.

## Step4:
Erode and Dilate the image.

## Step5:
End Program.


 
## Program:
```
# Developed By  : RAKSHITHA DEVI J
# Register Number: 212221230082

import cv2
import matplotlib.pyplot as plt 
from google.colab.patches import cv2_imshow
import numpy as np

# Create the Text using cv2.putText
img1 = np.zeros((100,270), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'RAKSHI',(5,70), font, 2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')

# Create the structuring element
kernel = np.ones((5,5),np.uint8)
erosion = cv2.dilate(img1,kernel,iterations = 1)
cv2.erode(img1, kernel)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode1 = cv2.erode(img1,kernel)
plt.imshow(image_erode1, 'gray')

# Dilate the image
image_dilate1 = cv2.dilate(img1, kernel)
plt.imshow(image_dilate1, 'gray')



```
## Output:

### Display the input Image
![image](https://github.com/Rakshithadevi/Implementation-of-Erosion-and-Dilation/assets/94165326/39b86a3b-2116-4097-8207-7a64001618bd)
### Display the Eroded Image
![image](https://github.com/Rakshithadevi/Implementation-of-Erosion-and-Dilation/assets/94165326/d19242e0-793b-48e5-9d01-2763b9c5becd)
### Display the Dilated Image
![image](https://github.com/Rakshithadevi/Implementation-of-Erosion-and-Dilation/assets/94165326/3c8f42db-1e7c-4d4e-9271-b74bea4ef9f8)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
