## EX.NO : 07
## Date : 12.05.2022
# <p align="center"> Edge-Detection</p>

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.
<br>


### Step2:
For performing edge detection on a image.

* Sobel
```python
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
```
* Laplacian
```python
Laplacian=cv2.Laplacian(img,cv2.CV_64F)
```
* Canny
```python
canny=cv2.Canny(img,120,150)
```

## Import the packages
```python
import cv2 
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("leaf.jpg",0)
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
img=cv2.GaussianBlur(img,(3,3),0)
plt.imshow(img)
plt.axis("off")
plt.show()

# SOBEL EDGE DETECTOR
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)

# LAPLACIAN EDGE DETECTOR
Laplacian=cv2.Laplacian(img,cv2.CV_64F)

# CANNY EDGE DETECTOR
canny=cv2.Canny(img,120,150)

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X axis')
plt.imshow(sobelx)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel Y axis')
plt.imshow(sobely)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Sobel X and Y axis')
plt.imshow(sobelxy)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian')
plt.imshow(Laplacian)
plt.show()

plt.figure(figsize=(20,20))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(img)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Canny')
plt.imshow(canny)
plt.show()

```
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

## Output
## SOBEL EDGE DETECTOR

![WhatsApp Image 2022-06-14 at 3 08 55 AM (5)](https://user-images.githubusercontent.com/75235704/173740049-64f5b7b7-23b2-4ae9-a6e1-10982964c076.jpeg)


![WhatsApp Image 2022-06-14 at 3 08 55 AM (4)](https://user-images.githubusercontent.com/75235704/173739993-5a897fe8-b30f-4559-839d-b47641baa9f0.jpeg)


![WhatsApp Image 2022-06-14 at 3 08 55 AM (3)](https://user-images.githubusercontent.com/75235704/173739827-88567072-cd38-409a-a30a-514a5eec73fa.jpeg)

## LAPLACIAN EDGE DETECTOR
![WhatsApp Image 2022-06-14 at 3 08 55 AM (2)](https://user-images.githubusercontent.com/75235704/173739764-5c8c81fa-54e7-44f0-bd56-e86d769479a9.jpeg)


## CANNY EDGE DETECTOR
![WhatsApp Image 2022-06-14 at 3 08 55 AM (1)](https://user-images.githubusercontent.com/75235704/173739661-16a34929-5f59-47f7-bf73-d4b908628303.jpeg)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
