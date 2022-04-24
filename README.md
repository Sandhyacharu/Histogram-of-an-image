# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image

## Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.

## Step3:
Display the histograms with their respective images.

## Step4:
Equalize the grayscale image.

## Step5:
Display the grayscale image

## Program:

### Developed By: N Sandhya Charu
### Register Number: 212220230041
```python3
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image = cv2.imread("butterfly.jpg")
plt.imshow(gray_image)
plt.show()
hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Grayscale value')
plt.ylabel('Pixel Count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

color_image=cv2.imread("venice.jpg")
plt.imshow(color_image)
plt.show()
hist1=cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image. 

gray_image = cv2.imread('butterfly.jpg',0)
equ=cv2.equalizeHist(gray_image)
cv2.imshow('Gray image',gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![image](https://user-images.githubusercontent.com/75235167/164967116-9996621d-58b3-4586-87db-b0d4fcd8afd2.png)
![image](https://user-images.githubusercontent.com/75235167/164967131-ffcc7d6f-e1e5-4f8d-9a43-ac0e08eb276e.png)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://user-images.githubusercontent.com/75235167/164967144-2c5059ac-8862-4de7-8205-f3e9c1b57ec2.png)
![image](https://user-images.githubusercontent.com/75235167/164967158-a348d5e8-2915-4429-9ac3-0bcfbb415f20.png)

### Histogram Equalization of Grayscale Image
![image](https://user-images.githubusercontent.com/75235167/164967181-d998f0b4-7a75-446b-8bb4-42f16969c64f.png)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
