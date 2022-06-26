## EX NO:04
## DATE:25.4.22
# <p align="center">Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.
<br>

### Step2:
Calculate the Histogram of Gray scale image and each channel of the color image.
<br>

### Step3:
Display the histograms with their respective images.
<br>

### Step4:
Equalize the grayscale image.
<br>

### Step5:
Display the grayscale image.
<br>

## Program:
```python
Developed By: Lishali R
Register Number: 212220230028

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('v.jfif')
plt.imshow(Gray_image)
plt.show()
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()


# Display the histogram of gray scale image and any one channel histogram from color image
Color_image=cv2.imread('v1.jfif')
plt.imshow(Color_image)
plt.show()
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()



# Write the code to perform histogram equalization of the image. 
Gray_image=cv2.imread('v.jfif',0)
equ=cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```



## Output:
### Input Grayscale Image and Color Image
![l11](https://user-images.githubusercontent.com/75237886/165021744-ffdd9c76-e980-4c39-beef-74a48d34ee82.jpg)

![l12](https://user-images.githubusercontent.com/75237886/165021747-974cee91-e6ef-419f-aa58-7cc3a9382d2b.jpg)

# Histogram of Grayscale Image and any channel of Color Image
![l21](https://user-images.githubusercontent.com/75237886/165021761-13565fc8-c1eb-4bbf-9c82-349961e147f2.jpg)
![l22](https://user-images.githubusercontent.com/75237886/165021791-780ff815-fe13-4440-9957-7f3038317e40.jpg)


### Histogram Equalization of Grayscale Image
![l3](https://user-images.githubusercontent.com/75237886/165022176-ac2e4127-5151-4353-9044-4e948b2e52e2.jpg)



## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
