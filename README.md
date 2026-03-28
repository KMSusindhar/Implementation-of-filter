# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Using Averaging Filter


### Step2
Using Weighted Averaging Filter

### Step3
Using Gaussian Filter

### Step4
Using Median Filter

### Step5
Using Laplacian Kernal

### Step6
Using Laplacian Operator

## Program:
### Developed By   : Susindhar K M
### Register Number: 212223040218


### 1. Smoothing Filters
1. Smoothing Filters
i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rose.png")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```

ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
iv)Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```
### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

ii) Using Laplacian Operator

```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()



```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter
<img width="1484" height="672" alt="image" src="https://github.com/user-attachments/assets/872d2969-e050-4b8b-a91d-b2864bba6518" />


ii)Using Weighted Averaging Filter
<img width="1483" height="666" alt="image" src="https://github.com/user-attachments/assets/bc50a0e3-3c21-489a-9d9f-30a706365ac0" />


iii)Using Gaussian Filter
<img width="1482" height="670" alt="image" src="https://github.com/user-attachments/assets/0152aae9-5929-476f-9a53-b0550da73102" />


iv) Using Median Filter
<img width="1479" height="668" alt="image" src="https://github.com/user-attachments/assets/63926015-5577-4072-ae72-806a4d6cb583" />


### 2. Sharpening Filters

i) Using Laplacian Kernal
<img width="1489" height="670" alt="image" src="https://github.com/user-attachments/assets/70a3a9c7-40b2-4fb9-ad60-d069eb0ad063" />

ii) Using Laplacian Operator
<img width="1769" height="665" alt="image" src="https://github.com/user-attachments/assets/8822bbb6-74b5-4eef-b039-843e59bc2cfa" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
