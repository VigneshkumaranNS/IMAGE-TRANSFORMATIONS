# EX-04 IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.



### Step2:
Load the image file in the program.



### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.



### Step4:
Display the modified image output.



### Step5:
End the program.

## Program:

```python
Developed By: VIGNESH KUMARAN N S
Register Number: 212222230171
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("bala.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()


# ii) Image Scaling
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("bala.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))

#iii)Image shearing
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("bala.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1, 0, 0],
                [0.5, 1, 0],
                [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis
plt.show()

#iv)Image Reflection

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("bala.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
# v)Image Rotation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("bala.jpg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
# vi)Image Cropping
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("bala.jpg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
cropped_img=input_image[100:300, 100:300]
plt.imshow(cropped_img)

```

## Output:
i)Image Translation
![image](https://github.com/VigneshkumaranNS/IMAGE-TRANSFORMATIONS/assets/119484483/e527dfa1-5d68-4cb9-adcc-932e2477644e)
![image](https://github.com/VigneshkumaranNS/IMAGE-TRANSFORMATIONS/assets/119484483/63be992b-2357-44a6-b00f-adbbd7e29462)


ii) Image Scaling
![image](https://github.com/VigneshkumaranNS/IMAGE-TRANSFORMATIONS/assets/119484483/b9f43655-88d8-4a13-9a47-5724d5338de3)


iii)Image shearing
![image](https://github.com/VigneshkumaranNS/IMAGE-TRANSFORMATIONS/assets/119484483/7c18fc0d-a574-448e-a5d3-3c64006eb9cd)


iv)Image Reflection
![4](https://github.com/BALA291/IMAGE-TRANSFORMATIONS/assets/120717501/852cb22b-1d10-4320-a857-68b3181dea44)



v)Image Rotation
![image](https://github.com/VigneshkumaranNS/IMAGE-TRANSFORMATIONS/assets/119484483/a0afdbd3-b8b4-4c63-969c-16e2e895e91f)



vi)Image Cropping
![image](https://github.com/VigneshkumaranNS/IMAGE-TRANSFORMATIONS/assets/119484483/dfcacb75-c9b9-444d-9a68-399ac0929830)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
