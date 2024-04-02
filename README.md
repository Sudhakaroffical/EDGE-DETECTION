# EDGE-DETECTION
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

## PROGRAM :
### DEVELOPED BY : SUDHAKAR K
### REGISTER NO : 212222240107
### Convert image to grayscale and remove noise
```P
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("flower dipt-6.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```p
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y AXIS :**
```p
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY AXIS :**
```p
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```p
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```p
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR


### SOBEL X AXIS :
![Screenshot 2024-04-02 114551](https://github.com/Sudhakaroffical/EDGE-DETECTION/assets/118622513/4eeb7ca1-5c82-462b-b320-db33aace2c55)






### SOBEL Y AXIS :

![Screenshot 2024-04-02 114617](https://github.com/Sudhakaroffical/EDGE-DETECTION/assets/118622513/94b282e8-1912-461e-ab5f-86262418f6b5)




### SOBEL XY AXIS :

![Screenshot 2024-04-02 114640](https://github.com/Sudhakaroffical/EDGE-DETECTION/assets/118622513/2ec2c85b-bbc8-4b55-b90c-ad957068aa52)



### LAPLACIAN EDGE DETECTOR :

![Screenshot 2024-04-02 114700](https://github.com/Sudhakaroffical/EDGE-DETECTION/assets/118622513/4b2b2ae3-ba7c-4647-a1d2-74bf478b2586)



### CANNY EDGE DETECTOR :

![Screenshot 2024-04-02 114716](https://github.com/Sudhakaroffical/EDGE-DETECTION/assets/118622513/728ce2fd-ee3a-4633-9afb-8384d6256175)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
