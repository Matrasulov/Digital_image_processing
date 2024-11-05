# Custom Trained Dataset with Cascade GUI trainer using Viola Jones algorithm

This repository contains a custom-trained cascade classifier XML dataset created with the **Cascade GUI Trainer** on Windows. This dataset was trained specifically to detect faces. It can be used for object detection tasks with OpenCV and other compatible libraries.



## **Dataset**: https://o365inha-my.sharepoint.com/:u:/g/personal/12204550_office_inha_ac_kr/EYmNshvUFyJFhecnhULfPqMB6jIiF-xyndCy6ETd7O0TCw?e=NTnkln




## Overview

The dataset was created as an XML classifier file using the **Cascade GUI Trainer** tool, which allows for the generation of Haar or LBP cascades through an intuitive graphical user interface on Windows. The classifier was trained with [number] stages and optimized for high accuracy and low false-positive rates. 

### Key Features
- **Custom Training**: Trained on specific images tailored for .
- **High Detection Rate**: Optimized to maximize hit rate while minimizing false alarms.
- **Easy Integration**: Compatible with OpenCV's `cv2.CascadeClassifier` for straightforward use.

## How to Use the Classifier

To use this custom cascade classifier in your project:
1. Download the XML file from this repository.
2. Place the XML file in your project directory.
3. Use the OpenCV `CascadeClassifier` in your code to load and apply the classifier.

