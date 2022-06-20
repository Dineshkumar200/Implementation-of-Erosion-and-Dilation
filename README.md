# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.
 
## Program:
```
/*
Developed by   : Dineshkumar V
Register Number: 212220230013
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,700),dtype='uint8')
font=cv2.FONT_ITALIC=3
img2=cv2.putText(img1,"Dineshkumar",(10,150),font,3,(255),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernal1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
erode=cv2.erode(img2,kernel)
cv2.imshow("Erosion1",erode)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Dilate the image
dilute=cv2.dilate(img2,kernel1)
cv2.imshow("Dilution",dilute)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:

### Display the input Image

![Screenshot 2022-05-25 202021](https://user-images.githubusercontent.com/75235789/170292309-4bd3ae7a-8bd6-418c-b966-4d9828d16be9.jpg)


### <br><br>Display the Eroded Image
![Screenshot 2022-05-25 202039](https://user-images.githubusercontent.com/75235789/170292354-4d359ef2-ef83-4945-9763-7a1b41c825b0.jpg)


### Display the Dilated Image
![Screenshot 2022-05-25 202021](https://user-images.githubusercontent.com/75235789/170292370-55970f22-b007-4ce7-8691-faa506c46b52.jpg)

## <br><br><br><br>Result
Thus the generated text image is eroded and dilated using python and OpenCV.
