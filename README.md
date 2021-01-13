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
listdir():It is used to get the list of all files and directories in the specified directory.
import cv2
import os
path=('C:\img')
imgs=[]
files=os.listdir(path)
for file in files:
 fpath=path+"\\"+file
 imgs.append(cv2.imread(fpath))
 i=0
 im=[]
 for im in imgs:
   im+=imgs[i]
   i=i+1
cv2.imshow("sum",im)
mean=im/len(files)
cv2.imshow("mean",mean) 
cv2.waitKey(0) 
Output:
![image](https://user-images.githubusercontent.com/72489647/104435265-07618980-5541-11eb-83c0-301cbd068559.png)
![image](https://user-images.githubusercontent.com/72489647/104435424-3841be80-5541-11eb-9f04-34126a5429f7.png)
4.Develop a program to convert the color image to gray scale and binary image.
Grayscaling:It is the process of converting an image from other color spaces.Eg:RGB,CMYK,HSV,etc to shades of gray .It varies between complete black and complete white.
Binary Image:It is the type of image where each pixel is black or white.Where 0 represents black and 1 represents white.
import cv2
image=cv2.imread('pic2.jpg')
cv2.imshow('Image',image)
cv2.waitKey(0)
grayImage = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('gray',grayImage)
cv2.waitKey(0)
ret,binaryImage= cv2.threshold(image, 100, 150, cv2.THRESH_BINARY)
cv2.imshow('binary',binaryImage)
cv2.waitKey(0)
cv2.destroyAllWindows()
Output:
![image](https://user-images.githubusercontent.com/72489647/104436455-7ab7cb00-5542-11eb-88d5-84126740db81.png)
![image](https://user-images.githubusercontent.com/72489647/104436644-b5b9fe80-5542-11eb-825c-f0fb73fcbaed.png)
![image](https://user-images.githubusercontent.com/72489647/104436816-e4d07000-5542-11eb-8c45-3470004a8fc0.png)
5.Develop a program to convert the given color image to different color spaces.
color spacing:color spaces are a way to represent the color channels present in the image that gives the image that particular hue.
import cv2
image=cv2.imread('pic3.jpg')
cv2.imshow('Image',image)
cv2.waitKey(0)
yuv_img = cv2.cvtColor(image,cv2.COLOR_RGB2YUV)
cv2.imshow('ychannel',yuv_img[:,:,0])
cv2.imshow('uchannel',yuv_img[:,:,1])
cv2.imshow('vchannel',yuv_img[:,:,2])
cv2.waitKey(0)
hsv_img = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('hchannel',hsv_img[:,:,0])
cv2.imshow('schannel',hsv_img[:,:,1])
cv2.imshow('vchannel',hsv_img[:,:,2])
cv2.waitKey(0)
Output:
![image](https://user-images.githubusercontent.com/72489647/104438424-d5eabd00-5544-11eb-8e1a-453eca48dfaa.png)
![image](https://user-images.githubusercontent.com/72489647/104438661-15190e00-5545-11eb-8c48-74a31cd3d2f9.png)
![image](https://user-images.githubusercontent.com/72489647/104438832-4b568d80-5545-11eb-844b-489839239153.png)
![image](https://user-images.githubusercontent.com/72489647/104439006-7b059580-5545-11eb-8c8e-a5d3ca988519.png)
![image](https://user-images.githubusercontent.com/72489647/104439171-aab49d80-5545-11eb-9741-71aa28e1534f.png)
![image](https://user-images.githubusercontent.com/72489647/104439335-d59ef180-5545-11eb-8cb9-98aed0bf7188.png)
![image](https://user-images.githubusercontent.com/72489647/104439462-fcf5be80-5545-11eb-8007-25e3ff5c473a.png)
6.Develop a program to create an image from 2D array (generate an array of random size).
2D array:Two-dimensional array is an array within an array.It is the type of array ,the position of an data element is referred by two indices instead of one.
