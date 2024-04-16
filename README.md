
# Implementation-of-Erosion-and-Dilation

## Aim

To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

   
## Algorithm:

### Step1:

Import necessary packages

### Step2:

Create an empty window and add text to it

### Step3:

create a structuring element

### Step4:

Do the operation

### Step5:

Show the output image

### Name: Sri Varshan P
### Register Number: 212222240104
 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
```

```py
#to read the color image
input_image_path='aakash.jpg'
color_image=cv2.imread(input_image_path)
```
```py
#convert the color image to grayscale
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
```
```py
#perform edge detection using Canny
edges=cv2.Canny(gray_image,100,200)
```
```py
#define the kernel size for erosion and dilation
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
```
```py
#perform erosion
erosion=cv2.erode(edges,kernel,iterations=1)

#perform dilation
dilation=cv2.dilate(edges,kernel,iterations=1)
```
```py

#Display original image
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
```
```py
#display all images
plt.figure(figsize=(7,7))

plt.subplot(2,2,1)
plt.imshow(gray_image,cmap='gray')
plt.title('Black and White Image')
plt.axis('on')

plt.subplot(2,2,2)
plt.imshow(edges,cmap='gray')
plt.title('Edge Segmentation')
plt.axis('on')

plt.subplot(2,2,3)
plt.imshow(erosion,cmap='gray')
plt.title('Erosion')
plt.axis('on')

plt.subplot(2,2,4)
plt.imshow(dilation,cmap='gray')
plt.title('Dilation')
plt.axis('on')

plt.show()
```
## Output:

### Display the input Image

![image](https://github.com/PSriVarshan/erosion-dilation/assets/114944059/3ec96dd8-a67d-491c-a54b-f5fe1d2860a8)


### Display the Eroded Image

![image](https://github.com/PSriVarshan/erosion-dilation/assets/114944059/b455b27e-b700-4f31-aebc-d21a19e49a08)

### Display the Dilated Image

![image](https://github.com/PSriVarshan/erosion-dilation/assets/114944059/7daa4114-6d9f-45a3-bb9d-7526231724e3)

### Full output

![image](https://github.com/PSriVarshan/erosion-dilation/assets/114944059/2e026aa9-1e94-4678-9bb2-046c70dad1ec)



## Result

### Thus the generated text image is eroded and dilated using python and OpenCV.
