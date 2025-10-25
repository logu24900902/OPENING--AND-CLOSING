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

## Program:
### NAME : LOGU R
### REG NO : 212224230141
``` Python
# Import necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt
from google.colab.patches import cv2_imshow

# i) Create the text using cv2.putText
img1 = np.zeros((300, 600), dtype='uint8')
font = cv2.FONT_ITALIC
img2 = cv2.putText(img1, "LOGU R", (5, 200), font, 2, (255), 6, cv2.LINE_AA)

cv2_imshow(img2)

# ii) Create structuring elements
kernel1 = cv2.getStructuringElement(cv2.MORPH_RECT, (11, 11))
kernel2 = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

# iii) Use Opening operation (Erosion followed by Dilation)
img_open = cv2.morphologyEx(img2, cv2.MORPH_OPEN, kernel2)
cv2_imshow(img_open)

# iv) Use Closing operation (Dilation followed by Erosion)
img_close = cv2.morphologyEx(img2, cv2.MORPH_CLOSE, kernel1)
cv2_imshow(img_close)



```
## Output:

### Display the input Image
<br>
<img width="641" height="373" alt="image" src="https://github.com/user-attachments/assets/39771d90-9fc4-44bb-ba7c-3241339d272e" />

<br>
<br>
<br>
<br>
<br>

### Display the result of Opening
<br>
<img width="745" height="381" alt="image" src="https://github.com/user-attachments/assets/cbc8a253-ae32-4ded-8fce-7d3923011b9f" />

<br>
<br>
<br>
<br>
<br>

### Display the result of Closing
<br>
<img width="685" height="382" alt="image" src="https://github.com/user-attachments/assets/45630120-08e8-4f7d-a0f3-5a504d33dd3c" />

<br>
<br>
<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
