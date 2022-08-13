# LGM_DataScience_Img_to_Pencil_sketch

from google.colab.patches import cv2_imshow

img = cv2.imread('dog.png', cv2.IMREAD_UNCHANGED)
cv2_imshow(img)

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2_imshow(img)

gray_image = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) 
#Show the new image gray_image
cv2_imshow(gray_image)

inverted_gray_image = 255 - gray_image

blurred_img = cv2.GaussianBlur(inverted_gray_image, (21,21),0) 
#Show the new image blurred_img
cv2_imshow(blurred_img)

inverted_blurred_img = 255 - blurred_img

pencil_sketch_IMG = cv2.divide(gray_image, inverted_blurred_img, scale = 256.0)

from google.colab.patches import cv2_imshow

img = cv2.imread('dog.png', cv2.IMREAD_UNCHANGED)
#Show the new image pencil sketch
cv2_imshow(pencil_sketch_IMG)
#Display the window infinitely until any keypress
cv2.waitKey(0)

img = cv2.imread('dog.png', cv2.IMREAD_UNCHANGED)
cv2_imshow(img)
gray_image = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) 
#Show the new image gray_image
cv2_imshow(gray_image)
blurred_img = cv2.GaussianBlur(inverted_gray_image, (21,21),0) 
#Show the new image blurred_img
cv2_imshow(blurred_img)
img = cv2.imread('dog.png', cv2.IMREAD_UNCHANGED)
#Show the new image pencil sketch
cv2_imshow(pencil_sketch_IMG)
#Display the window infinitely until any keypress
cv2.waitKey(0)
