# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
Step 1:
Import the necessary modules.

Step 2:
For performing smoothing operation on a image.

Average filter
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
Weighted average filter
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
Gaussian Blur
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
Median filter
median=cv2.medianBlur(image2,13)
Step 3:
For performing sharpening on a image.

Laplacian Kernel
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
Laplacian Operator
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
Step 4:
Display all the images with their respective filters.
## Program:
### Developed By   :  MEENA.S
### Register Number:212221240028
</br>
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Fawzil.jfif")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
```Python

kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
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
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
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
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
```Python

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
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
</br>

i) Using Averaging Filter
![Screenshot (56)](https://user-images.githubusercontent.com/94677128/167823918-80148e09-a78f-414c-a7cd-9f376287d4e8.png)



ii) Using Weighted Averaging Filter
![Screenshot (55)](https://user-images.githubusercontent.com/94677128/167823151-e1bc1243-f226-4d7e-9701-60bc11e616f7.png)

iii) Using Gaussian Filter
![Screenshot (54)](https://user-images.githubusercontent.com/94677128/167823544-c0952a07-a846-4f01-858e-133ca4cc8037.png)



iv) Using Median Filter
![Screenshot (57)](https://user-images.githubusercontent.com/94677128/167823338-b284d083-1837-4d41-9ce9-444546208c08.png)




### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![Screenshot (58)](https://user-images.githubusercontent.com/94677128/167823711-3bc05f07-70f0-400a-87c1-f403c3f403cd.png)



ii) Using Laplacian Operator
![Screenshot (59)](https://user-images.githubusercontent.com/94677128/167824266-3e2f2370-5511-4976-a73d-d9709ef9fea6.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
