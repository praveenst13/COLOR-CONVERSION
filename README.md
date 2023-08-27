# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>
mport cv2 library and upload the image or capture an image.

### Step2:
<br>
Read the saved image using cv2.imread("filename.jpg").

### Step3:
<br>
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) and similarly for other color formats.
### Step4:
<br>
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]).

### Step5:
<br>
Output the image using cv2.imshow("OUTPUT", image).

## Program:
```python
# Developed By:Praveen s
# Register Number:212222240077
# i) Convert BGR and RGB to HSV and GRAY
import cv2
houseImage = cv2.imread('k.jpeg')
cv2.imshow('212222240077_Praveens',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()




# ii)Convert HSV to RGB and BGR


import cv2
houseHSVImage = cv2.imread('k.jpeg')
cv2.imshow('212222240077_Praveens',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()


# iii)Convert RGB and BGR to YCrCb
import cv2
houseImage = cv2.imread('k.jpeg')
cv2.imshow('212222240077_Praveens',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()



# iv)Split and Merge RGB Image


import cv2
image = cv2.imread('k.jpeg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('212222240077_Praveens',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image
import cv2
image = cv2.imread('k.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('212222240077_Praveens',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow()



```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>

![dipt1](https://github.com/praveenst13/COLOR-CONVERSION/assets/118787793/dcdb9534-0ae7-484e-8bd5-95f5a85255e6)


<br>

### ii) HSV to RGB and BGR
<br>

![dipt2](https://github.com/praveenst13/COLOR-CONVERSION/assets/118787793/7a25d707-e17c-4f39-8400-a49a6fb0b84f)


<br>

### iii) RGB and BGR to YCrCb
<br>

![dipt3](https://github.com/praveenst13/COLOR-CONVERSION/assets/118787793/04955752-3ef7-4160-9ad3-52c4cce3d70a)


<br>

### iv) Split and merge RGB Image
<br>

![dipt4](https://github.com/praveenst13/COLOR-CONVERSION/assets/118787793/5f7e62fb-c271-4940-a644-46f474f69987)


<br>

### v) Split and merge HSV Image
<br>

![dipt5](https://github.com/praveenst13/COLOR-CONVERSION/assets/118787793/1d6df9fc-3262-467b-9706-e733adb63526)


<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
