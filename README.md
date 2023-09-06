# IMAGE-TRANSFORMATION

## Aim

To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:

Anaconda - Python 3.7

## Algorithm:

### Step1:

Import the necessary libraries and read the original image and save it a image variable.

### Step2:

Write a code to translation of the image.

### Step3:

Write a code for scaling of the image.

### Step4:

Write a code for shearing of the image.

### Step5:

Write a code for reflection of the image.

### Step6:

Write a code to rotation of the image.

### Step7:

Write a code to cropping of the image.

### Step8:

Display all the Transformed images.

## Program:
```
Developed By:DHANUMALYA D
Register Number:212222230030
```
i)Image Translation
```
import numpy as np
import matplotlib.pyplot as plt 
import cv2 as cv
```
```
#plotting of an image :
image = cv.imread("tree.jpg")
image = cv.cvtColor(image, cv.COLOR_BGR2RGB)

plt.axis("off")
plt.imshow(image)
plt.show()

#translation of an image :
rows,cols,dim = image.shape

M = np.float32([[1,0,100], [0,1,50],[0,0,1]])
translated_image= cv.warpPerspective(image, M, (cols, rows))

plt.axis("off")
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```
rows,cols,dim = image.shape

M_scale = np.float32([[1,0,0], [0,1.5,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.axis("off")
plt.imshow(scale_image)
plt.show()
```

iii)Image shearing
```
M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])

shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(shear_imagex)
plt.show()

plt.axis("off")
plt.imshow(shear_imagey)
plt.show()
```
iv)Image Reflection
```
M_x = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

M_y = np.float32([[-1,0,cols], [0,1,0],[0,0,1]])

ref_imagex= cv.warpPerspective(image, M_x, (cols, rows))
ref_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(ref_imagex)
plt.show()

plt.axis("off")
plt.imshow(ref_imagey)
plt.show()
```
v)Image Rotation
```
angle=np.radians(10)

matrix=np.float32([[np.cos(angle),-np.sin(angle),0],
                                [np.sin(angle),np.cos(angle),0],
                                [0,0,1]])

Rotated_image=cv.warpPerspective(image,matrix,(cols,rows))

plt.axis("off")
plt.imshow(Rotated_image)
```
vi)Image Cropping

```
crop_img = image[150:600 ,350:900]

plt.axis("off")
plt.imshow(crop_img)
plt.show()

```
## Output:
### i)Image Translation
![Screenshot from 2023-09-06 19-13-07](https://github.com/Dhanudhanaraj/IMAGETRANSFORMATION/assets/119218812/6ece8d91-357d-44ea-b2d1-b89efeabb820)


### ii) Image Scaling
![Screenshot from 2023-09-06 19-13-22](https://github.com/Dhanudhanaraj/IMAGETRANSFORMATION/assets/119218812/c4120491-e823-49f6-9d60-e47aeeebf897)


### iii)Image shearing
![Screenshot from 2023-09-06 19-13-41](https://github.com/Dhanudhanaraj/IMAGETRANSFORMATION/assets/119218812/79252871-7a6f-40f7-83b3-b1b5d159eec2)


### iv)Image Reflection

![Screenshot from 2023-09-06 19-13-41](https://github.com/Dhanudhanaraj/IMAGETRANSFORMATION/assets/119218812/6697c3af-709a-43b6-95c4-8c4df0940c49)



### v)Image Rotation

![Screenshot from 2023-09-06 19-13-54](https://github.com/Dhanudhanaraj/IMAGETRANSFORMATION/assets/119218812/c9284965-c006-42c0-9e7c-8e7d3e196b0e)


### vi)Image Cropping

![Screenshot from 2023-09-06 19-14-04](https://github.com/Dhanudhanaraj/IMAGETRANSFORMATION/assets/119218812/dbb74e2d-fd6f-49f0-bd4e-32fefc68823e)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
