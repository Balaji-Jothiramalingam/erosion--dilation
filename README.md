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

``

## Create the structuring element
``
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)



``
## Erode the image
``
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')



``
## Dilate the image
``
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')


``

## output:
## Display the input Image

![323307884-ae1f4652-8969-479e-a8aa-a8ad3e782858](https://github.com/user-attachments/assets/20f7260c-b41d-48c9-abd8-96336869f702)


## Display the Eroded Image
![323308135-027a641b-bce2-4bef-9b10-0a60a1152116](https://github.com/user-attachments/assets/ff490061-5b25-4563-9259-e8910600ddcf)

## Display the Dilated Image


![323308207-776a6718-a655-4167-b107-e43c0364b99c](https://github.com/user-attachments/assets/e83fc799-db50-4c18-b8d4-a39e2fb56a37)


## Result![Uploading 323308135-027a641b-bce2-4bef-9b10-0a60a1152116.png…]()

Thus the generated text image is eroded and dilated using python and OpenCV.
