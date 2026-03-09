# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: D Raju
# Register Number: 212224240128
```



### Input Grayscale Image and Color Image
```
import cv2
from matplotlib import pyplot as plt
#Load the color image
image = cv2.imread('image.png')
#Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
```
## Output:
<img width="404" height="525" alt="image" src="https://github.com/user-attachments/assets/d4e8be0c-ad5d-4a1d-8dde-21cb6446ad90" />



### Histogram of Grayscale Image
```
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
```
## Output:
<img width="792" height="584" alt="image" src="https://github.com/user-attachments/assets/2a9fbf2b-5d02-4ec8-b52c-4802072842de" />



### Histogram Equalization of Grayscale Image.
```
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='grey')
plt.title('Equalized Image')
plt.axis('off')
```
## Output:

<img width="422" height="515" alt="image" src="https://github.com/user-attachments/assets/d5c8fdf6-3e84-4f57-be10-f88899d17f68" />

## Equalized Histogram
```
hist_original = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```
## Output:
<img width="824" height="570" alt="image" src="https://github.com/user-attachments/assets/ad5fe670-d1e2-4466-bd80-3719a95c4ec8" />


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
