# Implementation of Erosion and Dilation Using OpenCV

## Aim

To implement morphological operations such as Erosion and Dilation on an image using Python and OpenCV.

## Learning Objectives

- Understand morphological image processing.
- Learn the concept of structuring elements.
- Perform image erosion using OpenCV.
- Perform image dilation using OpenCV.
- Compare the results of erosion and dilation.

## Software Used

- Anaconda – Python
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

1. Import the required libraries.
2. Create a blank image using NumPy.
3. Insert text onto the image using OpenCV.
4. Display the original image.
5. Create a structuring element (kernel).
6. Apply erosion to reduce the boundaries of foreground objects.
7. Apply dilation to increase the boundaries of foreground objects.
8. Display and compare the original, eroded, and dilated images.

## Program

### Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Step 2: Create a Blank Image

```python
img = np.zeros((300, 600), dtype=np.uint8)

plt.figure(figsize=(8, 4))
plt.imshow(img, cmap="gray")
plt.title("Blank Image")
plt.axis("off")
plt.show()
```

### Step 3: Insert Text into the Image

```python
cv2.putText(
    img,
    "EROSION AND DILATION",
    (30, 160),
    cv2.FONT_HERSHEY_SIMPLEX,
    1.2,
    255,
    3
)

plt.figure(figsize=(10, 4))
plt.imshow(img, cmap="gray")
plt.title("Original Image with Text")
plt.axis("off")
plt.show()
```

### Step 4: Create a Structuring Element (Kernel)

```python
kernel = np.ones((5, 5), np.uint8)

print("Structuring Element:")
print(kernel)
```

### Step 5: Perform Image Erosion

```python
erosion = cv2.erode(img, kernel, iterations=1)

plt.figure(figsize=(12, 5))

plt.subplot(1, 2, 1)
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(erosion, cmap="gray")
plt.title("Eroded Image")
plt.axis("off")

plt.show()
```

### Step 6: Perform Image Dilation

```python
dilation = cv2.dilate(img, kernel, iterations=1)

plt.figure(figsize=(12, 5))

plt.subplot(1, 2, 1)
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(dilation, cmap="gray")
plt.title("Dilated Image")
plt.axis("off")

plt.show()
```

### Step 7: Compare Erosion and Dilation

```python
images = [
    ("Original Image", img),
    ("Erosion", erosion),
    ("Dilation", dilation)
]

plt.figure(figsize=(14, 5))

for i, (title, result) in enumerate(images):
    plt.subplot(1, 3, i + 1)
    plt.imshow(result, cmap="gray")
    plt.title(title)
    plt.axis("off")

plt.tight_layout()
plt.show()
```

## Developed By

- **Name:** Shaajini N
- **Register No:** 212225040395

## Output

### 1. Original Image

- A blank image is created using NumPy.
- Text is inserted using OpenCV.
- The original text image is displayed.

### 2. Erosion

- The original image is displayed.
- Erosion is applied using a 5 × 5 kernel.
- The thickness of the characters is reduced.
- The boundaries of foreground objects shrink inward.

### 3. Dilation

- The original image is displayed.
- Dilation is applied using the same kernel.
- The thickness of the characters increases.
- The boundaries of foreground objects expand outward.

### 4. Comparison Output

- Original image, eroded image, and dilated image are displayed together.
- The differences between both morphological operations can be observed.

## Result

Thus, the morphological operations Erosion and Dilation were successfully implemented using Python and OpenCV. Erosion reduces the thickness of foreground objects, whereas Dilation increases their thickness.

## Output Screenshots

Add your Jupyter Notebook screenshots below:

- **Output 1:** Original Image with Text
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a498ad5d-e59e-4536-a661-df617ca602d9" />

- **Output 2:** Structuring Element
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/06c2f8c4-245e-4127-aef1-7a3104357755" />

- **Output 3:** Erosion Output
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/786e7108-9f50-4de4-840b-975b6eb80a0b" />

- **Output 4:** Dilation Output
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8b762765-2bd1-4d43-a585-0613303f2339" />

- **Output 5:** Comparison of Original, Erosion, and Dilation
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/9d41e292-a6e9-40b9-8520-c60418dfecac" />


