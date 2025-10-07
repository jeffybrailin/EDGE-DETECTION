## Name: Jeffy Brailin T
## Reg.No: 212223040076

# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
```

(np.float64(-0.5), np.float64(647.5), np.float64(1151.5), np.float64(-0.5))

```
<img width="296" height="510" alt="image" src="https://github.com/user-attachments/assets/f8d62a13-b09e-42dc-b96c-0024eb9756ae" />

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
```

(np.float64(-0.5), np.float64(647.5), np.float64(1151.5), np.float64(-0.5))
```
<img width="281" height="511" alt="image" src="https://github.com/user-attachments/assets/038c8687-dd55-4ad3-847e-6e4672eb6b4d" />


### LAPLACIAN EDGE DETECTOR

```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

```
(np.float64(-0.5), np.float64(647.5), np.float64(1151.5), np.float64(-0.5))
```

<img width="283" height="503" alt="image" src="https://github.com/user-attachments/assets/5fbe0501-123b-4bd7-b868-0c99a4d9781e" />

### CANNY EDGE DETECTOR

```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  

```
```

(np.float64(-0.5), np.float64(647.5), np.float64(1151.5), np.float64(-0.5))
```

<img width="296" height="518" alt="image" src="https://github.com/user-attachments/assets/6cdf2c67-4e27-4060-be5f-14523c9392b9" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
