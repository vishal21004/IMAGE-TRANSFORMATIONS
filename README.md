# IMAGE-TRANSFORMATIONS

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
Developed By:VISHAL M.A
Register Number:212222230177
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
![ORIG IMG 1](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/137e8096-23ed-4b79-8752-05ace5a883a1)
![IMG TRNSL](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/5a8cb9f7-3122-43c5-ba53-df2fa516b240)



### ii) Image Scaling
![IMG SCALING ](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/a6f46c27-c21e-4c68-aec0-bd19b8e8cf37)



### iii)Image shearing
![IMG SHEARING](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/be576915-f8d7-4de3-851a-53c8744a2aab)
![IMG SHEARING 2](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/ac342ff6-d52b-40f3-9148-1ae7f3e6ba31)


### iv)Image Reflection
![IG RFL1](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/32635bc8-047c-493b-a565-b1021d872d05)
![IMG RFL 2](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/a94f8998-af54-482d-8658-f552a645b948)


### v)Image Rotation
![IMG ROT 1](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/74976d2f-bc20-47c9-b7f1-cb80212c69cb)




### vi)Image Cropping
![IMG CRP](https://github.com/swedha333/IMAGE-TRANSFORMATIONS/assets/119560110/07cecc32-ddc0-4f2e-9a33-a170426456e8)



## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
