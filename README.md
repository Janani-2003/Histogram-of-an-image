# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

### Step3:
Display the histograms with their respective images.

### Step4:
Equalize the grayscale image.

### Step5:
Display the grayscale image.

## Program:
```python
# Developed By: JANANI.R
# Register Number:212221230039

import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

import cv2
import matplotlib.pyplot as plt
gray_image=cv2.imread('tj.jpg')
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.imshow(gray_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image

import cv2
import matplotlib.pyplot as plt
color_image=cv2.imread('tj.jpg')
hist=cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.imshow(color_image)
plt.show()
plt.figure()
plt.title("histogram")
plt.xlabel('colorscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()





# Write the code to perform histogram equalization of the image. 

import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread('tj.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()




```
## Output:
### Input Grayscale Image and Color Image

![op1](https://user-images.githubusercontent.com/94288340/229358691-ea068d2e-f287-4ca6-a0a6-a4d20894818c.png)

### Histogram of Grayscale Image and any channel of Color Image
![op2](https://user-images.githubusercontent.com/94288340/229358702-0757727f-cf34-43cc-b8c5-d88e4b6d9c43.png)

### Histogram Equalization of Grayscale Image
![2023-04-02 (1)](https://user-images.githubusercontent.com/94288340/229358727-43799d65-e485-4688-8e84-1b2029664143.png)

![2023-04-02](https://user-images.githubusercontent.com/94288340/229358730-011b2a05-2868-4629-bbe8-3f430e77939a.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
