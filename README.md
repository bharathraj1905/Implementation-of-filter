# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>
Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By   : Barathraj.B
### Register Number:212222230019
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("images (1).jpg")
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
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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

iv) Using Median Filter
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
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
plt.figure(figsize=(9,9))
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

![Screenshot 2024-03-19 112541](https://github.com/bharathraj1905/Implementation-of-filter/assets/121490575/d1f506f2-6d90-4f0f-b9af-1520fa10e321)


ii) Using Weighted Averaging Filter

![Screenshot 2024-03-19 112549](https://github.com/bharathraj1905/Implementation-of-filter/assets/121490575/f778dd3f-4df6-4755-9232-5b1d29fd9ce8)


iii) Using Gaussian Filter

![Screenshot 2024-03-19 112557](https://github.com/bharathraj1905/Implementation-of-filter/assets/121490575/1f1e3b0b-0a88-4480-9e94-eb6833e14316)


iv) Using Median Filter

![Screenshot 2024-03-19 112604](https://github.com/bharathraj1905/Implementation-of-filter/assets/121490575/2f5ce9a2-232b-4953-9d75-2b8572e2edbd)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-19 112613](https://github.com/bharathraj1905/Implementation-of-filter/assets/121490575/5ca7e3ea-f0e0-49c1-b49d-ab03e89267f3)


ii) Using Laplacian Operator

![Screenshot 2024-03-19 112621](https://github.com/bharathraj1905/Implementation-of-filter/assets/121490575/13f62786-d26e-4dc1-98cb-faf854e15a2b)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
