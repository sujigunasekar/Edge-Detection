# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step 1:
Import the required packages for further process.

## Step 2:
Read the image and convert the rgb image to gray scale image.

## Step 3:
Use filters for smoothing the image to reduce the noise.

## Step 4:
Apply the respective filters - Sobel, Laplacian edge detector and Canny edge detector.

## Step 5:
Display the filtered image using plot and imshow.

 
## Program:
# Program to find the solution for the given linear equations.

# Developed by: Suji.G
# RegisterNumber: 212222230152

``` 
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("download.jpeg")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```

# SOBEL EDGE DETECTOR
### SOBEL X:
```
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()
```

### SOBEL Y:
```
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()
```


### SOBEL XY:
```
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()
```


# LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()
```

# CANNY EDGE DETECTOR
```
canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()

```
## Output:
### SOBEL EDGE DETECTOR
### SOBEL X:

![Screenshot from 2023-04-12 14-27-46](https://user-images.githubusercontent.com/119559822/231408016-976e8e5e-cb60-4f26-8939-666feccc4c6c.png)


### SOBEL Y:

![Screenshot from 2023-04-12 14-29-12](https://user-images.githubusercontent.com/119559822/231408049-825120cc-12e3-485a-88da-50e035d8b9df.png)

### SOBEL XY: 

![Screenshot from 2023-04-12 14-29-22](https://user-images.githubusercontent.com/119559822/231410917-4e494464-8f23-4c01-a628-cf8201a5e601.png)


### LAPLACIAN EDGE DETECTOR
 

![Screenshot from 2023-04-12 14-29-29](https://user-images.githubusercontent.com/119559822/231411011-de60456e-5a02-4079-bd42-98b77286fdc0.png)

### CANNY EDGE DETECTOR

![Screenshot from 2023-04-12 14-29-36](https://user-images.githubusercontent.com/119559822/231411055-eac79eec-1fc5-4b4f-b6be-10e599880dbc.png)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
