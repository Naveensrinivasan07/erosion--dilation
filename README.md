# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages
### Step2:
Create the text using cv2.putText
### Step3:
Create the structuring element
### Step4:
Erode the image
### Step5:
Dilate  the image
 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt                                                                                                                                                                                                                                                                                           
# Create the Text using cv2.putText
image = cv2.imread("palase.jpeg")
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
eroded_image = cv2.erode(image, kernel, iterations=1)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Create the structuring element
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)

# Erode the image
plt.figure(figsize=(10, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")

# Dilate the image
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
plt.tight_layout()
plt.show()


```
## Output:

### Display the input Image
![Screenshot 2024-10-09 155328](https://github.com/user-attachments/assets/6cfa29cb-baff-4d40-aede-5affaef90e7e)

### Display the Eroded Image
![Screenshot 2024-10-09 155345](https://github.com/user-attachments/assets/2f4dfe57-25f8-45f1-96eb-b6094b64e1d6)

### Display the Dilated Image
![Screenshot 2024-10-09 155357](https://github.com/user-attachments/assets/76f39d2b-97fb-4e37-8ff2-ad9f2c5aec09)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.

