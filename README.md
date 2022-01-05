# KEERTHANA-IP-LAB-2022
# 1. Developed program to perform linear transformation on the image.

import cv2

image = cv2.imread('dog.jpg')

height, width = image.shape[:2]

center = (width/2, height/2)

rotate_matrix = cv2.getRotationMatrix2D(center=center, angle=90, scale=1)

rotated_image = cv2.warpAffine(src=image, M=rotate_matrix, dsize=(width, height))

cv2.imshow('Original image', image)

cv2.imshow('Rotated image', rotated_image)

cv2.waitKey(0)

cv2.imwrite('rotated_image.jpg', rotated_image)

![image](https://user-images.githubusercontent.com/96225389/148202039-799b814a-9dcb-452f-8b32-0717e553e6c4.png)

![image](https://user-images.githubusercontent.com/96225389/148202601-773e6485-a3a2-423c-a020-02b322f6de63.png)
