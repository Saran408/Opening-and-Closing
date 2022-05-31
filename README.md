# OPENING AND CLOSING

## AIM:
To implement Opening and Closing using Python and OpenCV.

## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Use Opening operation.
### Step 5:
Use Closing Operation.


## PROGRAM:
```
/*
Developed by   : SARAN M
Register Number: 212220230044
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'SARAN',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/75235427/171094486-3e284d1b-dd42-4f39-9935-1a2cf8109950.png)



### Display the result of Opening
![image](https://user-images.githubusercontent.com/75235427/171094512-baeeb94d-b6d1-47bf-867b-cf1045b14af5.png)



### Display the result of Closing
![image](https://user-images.githubusercontent.com/75235427/171094527-e8774ea6-0243-4b88-9c87-41e2a62635f5.png)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
