# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.
<br>

### Step2:
Translate the image using<br>Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))
<br>

### Step3:
Scale the image using<br>Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])<br>Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))
<br>

### Step4:
Shear the image using<br>Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])<br>Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))
<br>

### Step5:
Reflection of image can be achieved through the code<br>Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) <br>Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))
<br>

### Step6:
Rotate the image using Rotation_angle=np.radians(10)<br>Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]])<br>Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))
<br>

### Step7:
Crop the image using<br>cropped_image=org_img[10:350,320:560]
<br>

### Step8:
Display all the Transformed images.
<br>

## Program:
```python
Developed By: R ARUNRAJ
Register Number: 212220230004
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input= cv2.imread("tower.jpg")
input= cv2.cvtColor(input,cv2.COLOR_BGR2RGB)
cv2.imshow('Input',input)
plt.imshow(input)
cv2.waitKey(0)
plt.axis("on")
rows,cols,dim=input.shape
translation_matrix=np.float32(([1,0,100],[0,1,200],[0,0,1]))
translated_img=cv2.warpPerspective(input,translation_matrix,(cols,rows))
plt.axis("off")
plt.imshow(translated_img)

ii) Image Scaling
scaling_matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(input,scaling_matrix,(cols,rows))
plt.axis("off")
plt.imshow(scaled_img)

iii)Image shearing
shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
sheared_img=cv2.warpPerspective(input,shearing_matrix,(cols*2,int(rows*1.5)))
plt.axis("off")
plt.imshow(sheared_img)

iv)Image Reflection
reflection_matrix_col=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_col=cv2.warpPerspective(input,reflection_matrix_col,(cols,int(rows)))
plt.axis("off")
plt.imshow(reflected_img_col)
reflection_matrix_row=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
reflected_img_row=cv2.warpPerspective(input,reflection_matrix_row,(cols,int(rows)))
plt.axis("off")
plt.imshow(reflected_img_row)

v)Image Rotation
rotation_angle=np.radians(10)
rotation_matrix=np.float32([[np.cos(rotation_angle),-np.sin(rotation_angle),0],
                                [np.sin(rotation_angle),np.cos(rotation_angle),0],
                                [0,0,1]])
rotated_img=cv2.warpPerspective(input,rotation_matrix,(cols,(rows)))
plt.axis("off")
plt.imshow(rotated_img)

vi)Image Cropping
cropped_img=input[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_img)
```
## Output:
### i)Image Translation
![O1](https://user-images.githubusercontent.com/75235747/166108596-853bafb0-149d-4c0d-929d-0a8852b1b163.JPG)
<br>![O2](https://user-images.githubusercontent.com/75235747/166108602-71299ef3-8352-4a9f-a7f8-e46856c968de.JPG)

### ii) Image Scaling
![O3](https://user-images.githubusercontent.com/75235747/166108627-b6124f3e-9103-4d22-bfee-bb7139a9128f.JPG)

### iii)Image shearing
![O4](https://user-images.githubusercontent.com/75235747/166108660-cbaee4d8-17e8-4a09-84af-17ba767c98a9.JPG)

### iv)Image Reflection
![O5](https://user-images.githubusercontent.com/75235747/166108684-1448fc5b-84f0-4958-aee1-0d95fa5168d9.JPG)
<br>
![O6](https://user-images.githubusercontent.com/75235747/166108725-0974dc60-03d5-4d55-a5aa-df19630d59c7.JPG)

### v)Image Rotation
![O7](https://user-images.githubusercontent.com/75235747/166108806-50318075-9694-499d-9d6f-e529561fda26.JPG)

### vi)Image Cropping
![O8](https://user-images.githubusercontent.com/75235747/166108819-05f46977-cc04-47de-9ce3-c91dabc9357e.JPG)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
