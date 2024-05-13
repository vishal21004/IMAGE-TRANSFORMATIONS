# EX 04: IMAGE-TRANSFORMATIONS

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.
### Step2:
Translate the image using a function warpPerpective()
### Step3:
Scale the image by multiplying the rows and columns with a float value.
### Step4:
Shear the image in both the rows and columns.
### Step5:
Find the reflection of the image.
## Step 6:
Rotate the image using angle function.
## Program:
### Developed By:VISHAL M.A
### Register Number:212222230177
## Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("flor.jpeg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

##  Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
## Image shearing
```python 
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
## Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
## Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
## Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("flor.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation
![ORIG IMG 1](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/9a525d8b-6834-452a-bbd7-34981ac025bf)
![IMG TRNSL](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/4eb5a551-0182-4e7f-83e4-7bb2a0421e2d)


### ii) Image Scaling
![IMG SCALING ](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/c5b5e405-f0b6-431f-b1a9-d7c97fa10fb8)



### iii)Image shearing
![IMG SHEARING](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/195cd336-af12-48a9-ab41-67f5bf72535f)
![IMG SHEARING 2](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/e2d2fcb2-842d-4854-825f-187a24beb0bc)


### iv)Image Reflection
![IG RFL1](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/a7cd8af7-26c9-4a16-8090-88fa0af09fea)
![IMG RFL 2](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/0444a08d-990b-484a-b39c-7429a6bedc4b)


### v)Image Rotation
![IMG ROT 1](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/a72b74d5-a884-422b-8c4f-b1a40ae09817)



### vi)Image Cropping
![IMG CRP](https://github.com/vishal21004/IMAGE-TRANSFORMATIONS/assets/119560110/d231ddbf-ba1d-4cf7-bda6-e69d501e3c0b)



## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
