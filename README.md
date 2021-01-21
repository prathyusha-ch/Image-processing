# Image-processing
1.Develop a program to display grayscale image using read and write operations 
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
2.Develop a program to perform linear transformations on an image:Scaling and Rotation 
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
color space:color spaces are a way to represent the color channels present in the image that gives the image that particular hue.
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
import numpy as np
from PIL import Image
array=np.linspace(0,1,250*200)
mat=np.reshape(array,(250,200))
img=Image.fromarray(mat,'HSV')
img.show()
cv2.waitKey(0)
Output:
![image](https://user-images.githubusercontent.com/72489647/104440723-8ce83800-5547-11eb-93cd-f1af53bb8ae8.png)
7.Develop a program to find the neighbours of each element in the matrix.
import numpy as np
x=np.array([[5,7,2],[2,9,3],[1,2,4]])
print(x)
def neighbors(radius,rowNumber,columnNumber):
    return[[x[i][j]
           if i>=0 and i<len(x) and j>=0 and j<len(x[0]) else 0
           for j in range(columnNumber-1-radius,columnNumber+radius)]
          for i in range(rowNumber-1-radius,rowNumber+radius)]
neighbors(2,2,2)
Output:
![image](https://user-images.githubusercontent.com/72489647/104471290-ae493280-55e0-11eb-8a78-90fcab2bb7cf.png)
8 Write a program to find the sum of neighbour values in a matrix.
import numpy as np
def sumNeighbors(M,x,y):
    l = []
    for i in range(max(0,x-1),x+2): 
        for j in range(max(0,y-1),y+2):
            try:
                t = M[i][j]
                l.append(t)
            except IndexError:
                pass
    return sum(l)-M[x][y]

M = [[1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]] 

M = np.asarray(M)
N = np.zeros(M.shape)

for i in range(M.shape[0]):
    for j in range(M.shape[1]):
        N[i][j] = sumNeighbors(M, i, j)

print ("Original matrix:\n", M)
print ("Summed neighbors matrix:\n", N)
Output:
![image](https://user-images.githubusercontent.com/72489647/104448468-0e44c800-5552-11eb-9c27-1040b4e8cc21.png)

9.Write a C++ program to perform operator overloading.
void operator --():Overload the meaning of the -- operator.
#include <iostream>
using namespace std;
class TestClass {
private:
	int count;
public:
	TestClass() : count(5) {}
	void operator --() {
		count = count - 3;
	}
	void Display() { 

		cout << "Count: " << count; }
};

int main() {
	TestClass tc;
	--tc;
	tc.Display();
	return 0;
}
Output:
count: 2
void operator ++():Overload the meaning of the ++ operator.
#include <iostream>   
#include <iostream>   
using namespace std;
class OperatorOverload {
private:
	int x;

public:
	OperatorOverload() : x(10) {}
	void operator ++() {
		x = x + 2;
	}
	void Print() {
		cout << "The Count is: " << x;
		}
};
int main() {
	OperatorOverload ov;
	++ov;   
	ov.Print();
	return 0;
}
Output:
The count is: 12
Assignment operator overloading.
#include <iostream>
using namespace std;

int findsum(int n)
{
    int m1[10][10], m2[10][10], sum=0;
   cout << "Enter the elements of matrix: ";
   for (int i = 0;i<n;i++ ) {
     for (int j = 0;j < n;j++ ) {
       cin>>m1[i][j];
     }
   }
   for (int i = 0;i<n;i++ ) {
     for (int j = 0;j<n;j++ ) {
      m2[i][j]=m1[i][j];
     }
   }
   cout<<"Sum=";
   for (int i = 0;i<n;i++ ) {
      for (int j = 0;j<n;j++ ) {
        sum+=m2[i][j];
      }
   }
   return sum;
}
int main()

{
    int n=3;
    cout<<findsum(n);
    return 0;
}
Output:
Enter the elements of matrix
1 2 3
4 5 6
7 8 9
Sum=45
10.Develop a program to implement negative transformation of an image.
Negative Transformation:The second linear transformation is negative transformation,which is invert of identity transformation.In negative transformation, each value of the input image is subtracted from the L-1 and mapped onto the output image.
import cv2 
image=cv2.imread('abc.jpg')
cv2.imshow('Original',image)
img_neg=255-image
cv2.imshow('Negative',img_neg)
cv2.waitKey(0)
cv2.destroyAllWindows()
Output:
![image](https://user-images.githubusercontent.com/72489647/105329629-3356bd80-5b86-11eb-9ed2-86c92f8a5947.png)
![image](https://user-images.githubusercontent.com/72489647/105329845-757fff00-5b86-11eb-894b-77f8626c454f.png)
11.Develop a program to implement contrast enhancement of an image.
Contrast Enhancement:is a process that makes the image features stand out more clearly by making optimal use of the colors available on the display or output device,Contrast manipulations involve changing the range of values in an image in order to increase contrast.
from PIL import Image,ImageEnhance
im=Image.open('abcd.jpg')
im3=ImageEnhance.Color(im)
im3.enhance(2.0).show()
Output:
![image](https://user-images.githubusercontent.com/72489647/105331380-3fdc1580-5b88-11eb-961d-0cb2bb40f4a1.png)
12.Develop a program to implement thresholding of an image.
Image Thresholding:is a simple form of image segmentation.It is a way to create a binary image from a grayscale or full-color image. 
cv2.THRESH_BINARY: If pixel intensity is greater than the set threshold, value set to 255, else set to 0 (black).
cv2.THRESH_BINARY_INV: Inverted or Opposite case of cv2.THRESH_BINARY.
cv.THRESH_TRUNC: If pixel intensity value is greater than threshold, it is truncated to the threshold. The pixel values are set to be the same as the threshold. All other values remain the same.
cv.THRESH_TOZERO: Pixel intensity is set to 0, for all the pixels intensity, less than the threshold value.
cv.THRESH_TOZERO_INV: Inverted or Opposite case of cv2.THRESH_TOZERO.
import cv2  
import numpy as np  
image1 = cv2.imread('abcd.jpg')  
img = cv2.cvtColor(image1, cv2.COLOR_BGR2GRAY) 
ret, thresh1 = cv2.threshold(img, 120, 255, cv2.THRESH_BINARY) 
ret, thresh2 = cv2.threshold(img, 120, 255, cv2.THRESH_BINARY_INV) 
ret, thresh3 = cv2.threshold(img, 120, 255, cv2.THRESH_TRUNC) 
ret, thresh4 = cv2.threshold(img, 120, 255, cv2.THRESH_TOZERO) 
ret, thresh5 = cv2.threshold(img, 120, 255, cv2.THRESH_TOZERO_INV) 
cv2.imshow('Binary Threshold', thresh1) 
cv2.imshow('Binary Threshold Inverted', thresh2) 
cv2.imshow('Truncated Threshold', thresh3) 
cv2.imshow('Set to 0', thresh4) 
cv2.imshow('Set to 0 Inverted', thresh5)   
if cv2.waitKey(0) & 0xff == 27:  
    cv2.destroyAllWindows()
Output:
![image](https://user-images.githubusercontent.com/72489647/105332951-060c0e80-5b8a-11eb-8d45-0ef6274aa635.png)


    














