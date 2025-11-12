
# Ex NO: 10-OPENING--AND-CLOSING
### Name : vignesh R
### Reg No : 212223240177
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
### DEVELOPED BY: JANARTHANAN K
### REGISTER NO: 212223040072

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'JANARTHANAN K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image
<img width="658" height="154" alt="image" src="https://github.com/user-attachments/assets/2b5fed6b-f6a3-40f3-a5af-7a71bf965e83" />



### Display the result of Opening
<img width="688" height="161" alt="image" src="https://github.com/user-attachments/assets/bf950e6e-c9c5-438c-bcbd-a8b87bc866fe" />


### Display the result of Closing
<img width="625" height="157" alt="image" src="https://github.com/user-attachments/assets/04b10b69-2a65-4f87-9da4-6ba62ffa1a85" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
