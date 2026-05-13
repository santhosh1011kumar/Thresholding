# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.
# NAME : SANTHOSH KUMAR A
# REG NO : 212224230250
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program


# Load the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

```

# Read the Image and convert to grayscale
```
image = cv2.imread("C:\\Users\\admin\\Downloads\\My image.png")  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  

```



# Convert from BGR to RGB for display
```
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')
```
# Use Global thresholding to segment the image
```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

```

# Use Adaptive thresholding to segment the image

```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)


```


# Use Otsu's method to segment the image 
```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```



# Display the results

# Global Thresholding
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot
```
plt.tight_layout()
plt.show()

```


## Output

### Original Image

<img width="628" height="407" alt="image" src="https://github.com/user-attachments/assets/44a22612-198f-4ee7-a0c8-0044488c0234" />


### Global Thresholding

<img width="760" height="353" alt="image" src="https://github.com/user-attachments/assets/2e8f609d-850f-4aa4-ae34-68424c947a43" />

### Adaptive Thresholding
<img width="416" height="361" alt="image" src="https://github.com/user-attachments/assets/a7a368e6-ef45-4aad-88fd-7a392fef605b" />


### Optimum Global Thesholding using Otsu's Method

<img width="376" height="296" alt="image" src="https://github.com/user-attachments/assets/94494c3d-7735-4d51-8ad6-d92dfe2c5d74" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
