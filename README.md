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


