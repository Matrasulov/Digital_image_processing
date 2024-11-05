# Custom Trained Dataset with Cascade GUI trainer using Viola Jones algorithm

This repository contains a custom-trained cascade classifier XML dataset created with the **Cascade GUI Trainer** on Windows. This dataset was trained specifically to detect faces. It can be used for object detection tasks with OpenCV and other compatible libraries.



## **Dataset**: https://o365inha-my.sharepoint.com/:u:/g/personal/12204550_office_inha_ac_kr/EYmNshvUFyJFhecnhULfPqMB6jIiF-xyndCy6ETd7O0TCw?e=NTnkln




## Overview

The dataset was created as an XML classifier file using the **Cascade GUI Trainer** tool, which allows for the generation of Haar or LBP cascades through an intuitive graphical user interface on Windows. The classifier was trained with [number] stages and optimized for high accuracy and low false-positive rates. 

### Key Features
- **Custom Training**: Trained on specific images tailored for [object type or specific use case].
- **High Detection Rate**: Optimized to maximize hit rate while minimizing false alarms.
- **Easy Integration**: Compatible with OpenCV's `cv2.CascadeClassifier` for straightforward use.

## How to Use the Classifier

To use this custom cascade classifier in your project:
1. Download the XML file from this repository.
2. Place the XML file in your project directory.
3. Use the OpenCV `CascadeClassifier` in your code to load and apply the classifier.

### Example Code

```python
import cv2

# Load your custom cascade classifier
custom_cascade = cv2.CascadeClassifier('path_to_your_cascade.xml')

# Load an image
image = cv2.imread('path_to_image.jpg')
gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Detect objects using the custom cascade
objects = custom_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=5, minSize=(24, 24))

# Draw rectangles around detected objects
for (x, y, w, h) in objects:
    cv2.rectangle(image, (x, y), (x + w, y + h), (255, 0, 0), 2)

# Display the result
cv2.imshow('Custom Cascade Detection', image)
cv2.waitKey(0)
cv2.destroyAllWindows()


