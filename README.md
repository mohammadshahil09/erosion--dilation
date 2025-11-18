# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale


### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.

 
## Program:
## Developed by: MOHAMMAD SHAHIL
## Reg NO: 212223240044

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HARIKA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image
<img width="648" height="130" alt="Screenshot 2025-11-18 083011" src="https://github.com/user-attachments/assets/eb727579-a0c0-4cec-ad0c-c2ce236a8562" />

### Display the Eroded Image
<img width="646" height="126" alt="Screenshot 2025-11-18 083032" src="https://github.com/user-attachments/assets/2d1a5ad9-66ef-4ced-9414-6d6984f4fe03" />

### Display the Dilated Image
<img width="647" height="115" alt="Screenshot 2025-11-18 083158" src="https://github.com/user-attachments/assets/7a499b6f-c7e2-431f-a7ad-e8ed3e8751c1" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
