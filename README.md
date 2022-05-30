# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages.

### Step 2:
Create the text image using cv2.putText.

### Step 3:
Then create the structuring element for opening and closing.

### Step 4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:
Plot the images using plt.imshow.

## Program:

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"sri harish",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')


# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```
## Output:

### Display the input Image
![image](https://user-images.githubusercontent.com/75241366/170996226-ee464309-6f88-4810-ba4b-871d6af07c14.png)


### Display the result of Opening
![image](https://user-images.githubusercontent.com/75241366/170996293-c1577de3-ac5b-4798-add7-820ec0894fc9.png)

### Display the result of Closing
![image](https://user-images.githubusercontent.com/75241366/170996391-d3292f99-7a95-4dab-b02e-7bc66ecef471.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
