# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step 2:
Translate the image.
<br>

### Step 3:
Scale the image.
<br>

### Step 4:
Shear the image.
<br>

### Step 5:

Reflect of image.
<br>

### Step 6:
Rotate the image.
<br>

## Program:
```python
Developed By: Sithi Hajara I
Register Number: 212221230102
```
i)Image Translation
```python
#Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("bunny.png")
input_image = cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M = np.float32([[10, 0, 100],
                [0, 10, 200],
                [0, 0, 10]])
translated_image = cv2.warpPerspective (input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```python
#Image Scaling

S=np.float32([[4,0,0],[0,4,0],[0,0,4]])
scaled_image=cv2.warpPerspective(input_image,S,(cols*4,rows*4))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```
iii)Image shearing
```python
#Image shearing

M_x = np.float32([[1, 0.5, 0],
                  [0, 1 ,0],
                  [0, 0 , 1]])
M_y= np.float32([[1, 0, 0],
                 [0.5, 1, 0],
                 [0, 0, 1]])
sheared_img_xaxis = cv2.warpPerspective (input_image,M_x,(int(cols*1.5), int(rows *1.5))) 
sheared_img_yaxis = cv2.warpPerspective (input_image,M_y, (int(cols*1.5), int(rows *1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()

plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
iv)Image Reflection
```python
#Image Reflection

M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```

v)Image Rotation
```python
#Image Rotation

angle=np.radians(80)
M=np.float32([[np.sin(angle),-(np.cos(angle)),0],
               [np.cos(angle),np.sin(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
vi)Image Cropping
```python
#Image Cropping
cropped_img=input_image[23:80,20:60]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
<br>

![image](https://user-images.githubusercontent.com/94219582/232054749-51b4221f-0415-4303-b430-c1a57daa243b.png)


<br>

![image](https://user-images.githubusercontent.com/94219582/232054911-73a3e1a0-8029-428c-8c68-2e17615d9a70.png)


### ii) Image Scaling

![image](https://user-images.githubusercontent.com/94219582/232055004-56c7de37-9c44-4aae-b7c5-255de83fa04c.png)



### iii)Image shearing



![image](https://user-images.githubusercontent.com/94219582/232055103-3993b169-d048-4ec7-9928-183e5d7dde44.png)


<br>

![image](https://user-images.githubusercontent.com/94219582/232055202-f5dc1a6f-4bcd-48c6-b381-7233ecbffe13.png)



### iv)Image Reflection
<br>

![image](https://user-images.githubusercontent.com/94219582/232055290-335d80d1-dc3a-4708-97dc-4ec39b0c94c9.png)



<br>

![image](https://user-images.githubusercontent.com/94219582/232055367-c2d8bb24-3b59-4a82-8f48-9576eba2f03f.png)



### v)Image Rotation

![image](https://user-images.githubusercontent.com/94219582/232055491-e36bede8-82f5-4763-a26b-24e4484d700e.png)




### vi)Image Cropping

![image](https://user-images.githubusercontent.com/94219582/232055606-3e85eac8-9ba1-48e4-bd33-6c1f6863d51d.png)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
