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

Create the Text using cv2.putText
### Step3:

Create the structuring element
### Step4:

Use Opening operation
### Step5:
Use Closing Operation

 
## Program:

Developed by: Divyadharshini.A

Register Number:212222240027

``` Python
# Import the necessary packages

import numpy as np
import cv2
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Datascientist',(5,70), font,2,(255),5,cv2.LINE_AA)
```

# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```

# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")

```
## Output:

### Display the input Image

![image](https://github.com/divyadharshiniddanbarasu/OPENING--AND-CLOSING/assets/119393424/d23e9026-0d13-4385-9453-7a1833f1556b)

### Display the result of Opening

![image](https://github.com/divyadharshiniddanbarasu/OPENING--AND-CLOSING/assets/119393424/adc1ffd3-0079-45b4-9e22-c8cc00813b46)


### Display the result of Closing

![image](https://github.com/divyadharshiniddanbarasu/OPENING--AND-CLOSING/assets/119393424/5436a2f3-c121-499d-9b0a-49b86a912bef)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
