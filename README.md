# Image-processing
1.Develop a program to display Grayscale image using read and write operations 
Grayscaling:It is the process of converting an image from other color spaces.Eg:RGB,CMYK,HSV,etc to shades of gray .It varies between complete black and complete white.
import cv2
image= cv2.imread('pic2.jpg')
cv2.imshow('original',image)
cv2.waitKey(0)
gray_image=cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('Grayscale',gray_image)
cv2.imwrite('graying.jpg',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
Output:
![image](https://user-images.githubusercontent.com/72489647/104427696-6cfd4800-5538-11eb-9bda-405c09955a56.png)
![image](https://user-images.githubusercontent.com/72489647/104428096-e432dc00-5538-11eb-99a8-1267a228eefe.png)
2.Develop a program to perform linear transformation of an image. 
Scaling:It is the process of resizing a digital image.We can perform scaling on an image using resize() method.
import cv2
import numpy as np
src=cv2.imread('pic2.jpg')
img=cv2.imshow('Image',src)
cv2.waitKey(0)
scale_p=200
width=int(src.shape[1]*scale_p/100)
height=int(src.shape[0]*scale_p/100)
dsize=(width,height)
result=cv2.resize(src,dsize)
cv2.imshow('scaling',result)
cv2.waitKey(0)
cv2.destroyAllwindows()
Output:
![image](https://user-images.githubusercontent.com/72489647/104429834-e5fd9f00-553a-11eb-98e1-92087eae073c.png)
![image](https://user-images.githubusercontent.com/72489647/104430277-53113480-553b-11eb-8b21-85237a0fb184.png)
Rotating an Image: The image rotation needs angle as parameter to get the image rotated.
import cv2
import numpy as np
src=cv2.imread('pic3.jpg')
image=cv2.imshow('Image',src)
windowsname=image
image=cv2.rotate(src,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow(windowsname,image)
cv2.waitKey(0)
Output:
![image](https://user-images.githubusercontent.com/72489647/104432088-7f2db500-553d-11eb-861a-a03e3038d634.png)
![image](https://user-images.githubusercontent.com/72489647/104432324-c2882380-553d-11eb-9de1-3209b82f6981.png)
3.Develop a program to find the sum and mean of a set of images. 
a.	Create ‘n’ number of images and read them from the directory and perform the operations.





