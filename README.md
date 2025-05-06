# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
Step1:
Import the necessary packages

Step2:
Create the Text using cv2.putText

Step3:
Create the structuring element

Step4:
Use Opening operation

Step5:
Use Closing Operation
## Program:

``` Python
#TRISHA PRIYADARSHNI PARIDA
#212224230293
#exp-10-Opening & Closing
import cv2
import numpy as np
import matplotlib.pyplot as plt
#i) Create the Text using cv2.putText
img1=np.zeros((300,600),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Trisha G",(5,100),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()
#ii) Create the structuring element
#kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
#kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(11,11))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(5,5))
#iii) Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()
#iv) Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
![1](https://github.com/user-attachments/assets/7febb85a-114b-4931-8dfe-2222a68224db)


### Display the result of Opening
![2](https://github.com/user-attachments/assets/4c298fa2-ac73-47bb-8916-d232c49dc953)

### Display the result of Closing
![3](https://github.com/user-attachments/assets/5f5c5b4f-5b4b-4365-8d06-a4807cf1b2cf)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
