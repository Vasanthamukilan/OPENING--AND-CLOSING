# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

## Program:
```
Developed by: Vasanthamukilan M
Register Number: 212222230167
```
### Display the input Image
```python
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'Krishnaraj', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
### Create ths structured element
```python
struct_ele = np.ones((9, 9), np.uint8)
```
### Display the result of Opening
```python
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
### Display the result of Closing
```python
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
## Output:

### Display the input Image

<img height=20% width=70% src="https://github.com/Vasanthamukilan/OPENING--AND-CLOSING/assets/119559694/8ef9f8de-59f5-4f6c-8ce7-6b8087ec257c">

### Display the result of Opening

<img height=20% width=70% src="https://github.com/Vasanthamukilan/OPENING--AND-CLOSING/assets/119559694/859a5e59-b9f8-4c94-a006-4cb199de0afb">


### Display the result of Closing
<img height=20% width=70% src="https://github.com/Vasanthamukilan/OPENING--AND-CLOSING/assets/119559694/fa9391c3-ef0b-4588-9f4b-562126545bd7">

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
