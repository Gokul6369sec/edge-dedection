# edge-detection-opencv

## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Sobel operator** using OpenCV to detect edges.

### Step 5:
Apply **Prewitt operator** using custom kernels.

### Step 6:
Apply **Roberts operator** using custom kernels.

### Step 7:
Apply **Laplacian operator** using OpenCV.

### Step 8:
Apply **Canny edge detector** using OpenCV.

### Step 9:
Display all edge-detected images for comparison.

---

## Developed By

- **Name:** GOKULAN R
- **Register No:** 212224230076

---

## Output

###  Sobel Edge Detector
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('spi.jpg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="481" height="409" alt="image" src="https://github.com/user-attachments/assets/928f7ddc-89a7-46c0-9191-affe52bc0b4e" />
<img width="481" height="409" alt="image" src="https://github.com/user-attachments/assets/1f3c83ad-38c4-4be4-8c13-8ba8dcf08d7f" />


###  Laplacian Edge Detector
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="481" height="409" alt="image" src="https://github.com/user-attachments/assets/cd5b8bec-7049-4920-aa32-21ed5a94c2cb" />





###  Canny Edge Detector
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```

<img width="481" height="409" alt="image" src="https://github.com/user-attachments/assets/66b65822-def8-4c23-9654-5ec4822e6b9a" />




## Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
