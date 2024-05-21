# Gray Scale Morphology
## AIM:

  To implement real-time fracture detection using grayscale morphology.
  
## ALGORITHM:

1.Read and Prepare the Image.

2.Apply Erosion Morphological Operation.

3.Use cv2.erode to apply the erosion operation with the kernel.

4.Subtract the eroded image from the original image using cv2.absdiff.

5.Create subplots using Matplotlib to display the original, eroded, and fractures images.

6.Show the images using plt.show with appropriate titles.

## PROGRAM:
```
Developed By : JANANI.S
Reg. No. : 212222230049
```
```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
frac=cv2.imread('bone.jpg')

# Define the structuring element for erosion
kernel = np.ones((11,11),np.uint8)

# Apply erosion morphological operation
eroded_image = cv2.erode(frac, kernel, iterations=1)

plt.subplot(1, 2, 1)
plt.imshow(frac, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')

plt.show()

import cv2
import matplotlib.pyplot as plt
import numpy as np
frac=cv2.imread('bone.jpg')

# Define the structuring element for erosion
kernel = np.ones((11,11),np.uint8)

# Apply erosion morphological operation
eroded_image = cv2.erode(frac, kernel, iterations=1)

# Subtract eroded image from original to get fractures
fractures = cv2.absdiff(frac,eroded_image)

plt.subplot(1, 2, 1)
plt.imshow(frac, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image')
plt.axis('off')

plt.subplot(1, 2, 2)
plt.imshow(eroded_image, cmap='gray')
plt.title('Eroded Image (flat)')
plt.axis('off')

plt.show()
```
## OUTPUT:
![Screenshot 2024-05-20 195622](https://github.com/Jenishajustin/Gray_Scale_Morphology/assets/119405070/9b68de4e-751a-4306-b51b-cda4c20b6ee6)
![Screenshot 2024-05-20 195644](https://github.com/Jenishajustin/Gray_Scale_Morphology/assets/119405070/843b1b73-d51d-47bd-ba43-cf6642dc2a57)

## RESULT:
   Hence the python program to implement real-time fracture detection using grayscale morphology is successfully implemented.
