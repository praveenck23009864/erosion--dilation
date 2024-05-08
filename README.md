## EX 09 Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
## Program:
```
Developed By: Pravinrajj G.K
Register No: 212222240080
```
``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((90,450),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'ONE PIECE',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')

# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)

# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

# Dilate the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://github.com/Pravinrajj/erosion--dilation/assets/117917674/7e4703b0-0ed6-4832-862c-328a2b66583b)

### Display the Eroded Image
![image](https://github.com/Pravinrajj/erosion--dilation/assets/117917674/3d9abce5-580b-405c-a711-27df38c933af)

### Display the Dilated Image
![image](https://github.com/Pravinrajj/erosion--dilation/assets/117917674/0685de82-1331-4bd2-ab0d-d6e4544525fb)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
