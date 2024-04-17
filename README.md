# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:

Import the necessary packages

### Step2:

Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:

Similarly, perform closing operation and display the result

### Step5:

The program should be executed in google colab.
 
## Program:
DEVELOPED BY:MARELLA HASINI

REGISTER NUMBER:212223240083
``` Python
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'IMAGE',(5,70), font,2,(255),5,cv2.LINE_AA)


# Create the structuring element
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")



# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:

### Display the input Image
![OUTPUT](<Screenshot 2024-04-17 085126.png>)

### Display the result of Opening
![OUTPUT](<Screenshot 2024-04-17 085133.png>)

### Display the result of Closing
![OUTPUT](<Screenshot 2024-04-17 085137.png>)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
