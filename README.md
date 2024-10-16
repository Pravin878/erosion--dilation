# EX-09:Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1:Initialize an Empty Image:

Create a black image of size 100x600 pixels.
### Step-2:Add Text to the Image:

Use a specified font to write the word "Dhiyaneshwar" on the image at a defined position.
### Step-3:Display the Original Image:

Show the image containing the text without axis labels.
### Step-4:Create Structuring Elements:

Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5:Erode the Image:

Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6:Dilate the Image:

Apply dilation to the original image using the same structuring element to increase the size of white regions.

 
## Program:
```
Developed By: pravin kumar G
Reference Number : 212222230109
``` 
# Import the necessary packages

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```python
img = np.zeros((100,600),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'HARIHARAN A',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
## Output:
![WhatsApp Image 2024-10-16 at 14 30 05_de08d5ac](https://github.com/user-attachments/assets/b59f31f3-bf28-4863-85ca-e1052c33db62)




# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
## Output:

![WhatsApp Image 2024-10-16 at 14 30 32_793ee847](https://github.com/user-attachments/assets/e11dbf53-6bda-458a-9341-cdbb710db7a1)






# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
## Output:

![WhatsApp Image 2024-10-16 at 14 31 01_9625cbec - Copy](https://github.com/user-attachments/assets/590081eb-1508-42d3-a476-cf95e17790ec)




# Dilate the image

```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:
![WhatsApp Image 2024-10-16 at 14 31 28_c2655c2d](https://github.com/user-attachments/assets/fef97370-6397-49a2-9cdc-5b35ca43809d)




## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
