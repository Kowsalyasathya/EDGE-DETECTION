# EXP 6 EDGE DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.


## Program:
### IMPORT PACKAGES AND LOAD IMAGES:
```
DEVELOPED BY: KOWSALYA M
REGISTER NUMBER: 212222230069

import cv2
import matplotlib.pyplot as plt

img=cv2.imread("mountain.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
I) SOBEL X:
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
ii) SOBEL Y:
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
iii) SOBEL XY:
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### ORIGINAL IMAGE:
![mountain](https://github.com/user-attachments/assets/90af4cd5-c239-46f0-a1b8-3a9afcfa613c)

### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/63c91835-ed98-4a57-a01a-867d4c1adcff)


![image](https://github.com/user-attachments/assets/c8b78c17-75a5-4490-9a17-001516334396)


![image](https://github.com/user-attachments/assets/ca24cedc-0645-48b5-a6f8-ede6b376d3da)

### LAPLACIAN EDGE DETECTOR:

![image](https://github.com/user-attachments/assets/b5b77c3a-2e5b-4979-8472-96fcb9121726)


### CANNY EDGE DETECTOR:

![image](https://github.com/user-attachments/assets/853304d1-dd67-4a2a-bc80-c516996f035c)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
