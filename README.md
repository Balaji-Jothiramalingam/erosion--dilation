## EX-09:Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV
## Algorithm:
## Step-1:Initialize an Empty Image:
Create a black image of size 100x600 pixels.

## Step-2:Add Text to the Image:
Use a specified font to write the word "Lifestyle" on the image at a defined position.

## Step-3:Display the Original Image:
Show the image containing the text without axis labels.

## Step-4:Create Structuring Elements:
Define a structuring element for morphological operations (e.g., a cross-shaped kernel).

## Step-5:Erode the Image:
Apply erosion to the image using the defined structuring element to reduce the size of white regions.

## Step-6:Dilate the Image:
Apply dilation to the original image using the same structuring element to increase the size of white regions.

## Program:
Developed By: BALAJI J
Reference Number :212221243001

## Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
``
img = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Lifestyle',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')

![380368334-d77d3259-4bdd-4bf4-a6cb-6b90a93e2002](https://github.com/user-attachments/assets/0b63420b-48b8-4e6d-b44b-c9c455f5b302)

``
## Create the structuring element
``
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)

![380368521-b8de1154-b574-4aee-9017-fd28629a6e97](https://github.com/user-attachments/assets/964868a7-cdc0-4785-b6a7-b617d85eb18e)

``
## Erode the image
``
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

![380368332-29d2f9f7-4add-4160-8024-33872463de66](https://github.com/user-attachments/assets/52819b44-cc20-4426-8358-0cd846c3e693)


``
## Dilate the image
``
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

![380368333-32f9e2cd-5fbc-4e39-bba0-a7806c7e1439](https://github.com/user-attachments/assets/a3cfd8cc-635a-44bb-8f48-9236c82ea70e)


``
## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
