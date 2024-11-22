## Ex 9 - Implementation of Erosion and Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm:
## Step 1:
Import the required libraries.

## Step 2:
Create a text image using cv2.putText().

## Step 3:
Define a structuring element for the erosion and dilation operations.

## Step 4:
Apply erosion to the image using cv2.erode().

## Step 5:
Apply dilation to the image using cv2.dilate().

## Step 6:
Display the original, eroded, and dilated images.

## Program:
Developed by : BALAJI J
Reg.no : 212221243001
# Import the necessary packages
```
import cv2
import numpy as np
image = np.zeros((300, 600), dtype="uint8")
```

# Create the Text using cv2.putText
```
cv2.putText(image, 'Image Processing', (30, 150), cv2.FONT_HERSHEY_SIMPLEX, 2, (255, 255, 255), 5)
```
# Create the structuring element
```
kernel = np.ones((5,5), np.uint8)
```

# Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```

# Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)

cv2.imshow('Input Image', image)
cv2.imshow('Eroded Image', eroded_image)
cv2.imshow('Dilated Image', dilated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
## Display the input Image
![image](https://github.com/user-attachments/assets/0d747cbd-d9db-43d0-807a-7eacd52f12a3)


## Display the Eroded Image
![image](https://github.com/user-attachments/assets/fc7346a5-17fb-4489-9f03-d15ef3020968)


## Display the Dilated Image
![image](https://github.com/user-attachments/assets/c8327468-3be3-4ac3-9b7e-006c92494c88)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
