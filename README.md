```
 NAME : MUKESH P
 REG NO : 212222240068
 ASSIGNMENT -> 29.10.24
```
#  EX-1: APOLLO 11 LAUNCH
# CODE

```
  import cv2
  from matplotlib import pyplot as plt
  image = cv2.imread('roc.jpg', cv2.IMREAD_GRAYSCALE)
  height, width = image.shape
  print("Width:", width)
  print("Height:", height)
  plt.figure(figsize=[10, 10])
  plt.imshow(image, cmap='gray')
  plt.axis('off') 
  plt.show()
  cv2.imwrite('roc.png', image)
  image = cv2.imread('roc.jpg')
  text = 'Apollo 11 Saturn V Launch, July 16, 1969'
font_face = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
font_thickness = 2
text_color = (0, 255, 0) 
text_size, _ = cv2.getTextSize(text, font_face, font_scale, font_thickness)
text_x = (image.shape[1] - text_size[0]) // 2
text_y = image.shape[0] - 50  
cv2.putText(image, text, (text_x, text_y), font_face, font_scale, text_color, font_thickness)
rect_color = (255, 0, 255)  # Magenta color in BGR
top_left = (500, 100)  # Coordinates adjusted to encompass the tower and rocket
bottom_right = (700, 600)  # Coordinates adjusted to encompass the tower and rocket
cv2.rectangle(image, top_left, bottom_right, rect_color, 5)
plt.figure(figsize=[12, 12])
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.axis('off')
plt.show()
```
# OUTPUT
```
Width: 1280
Height: 720
```
![ROC1](https://github.com/user-attachments/assets/4d4bb263-5bc0-4906-9300-888a7388c771)

```
True
```
```array([[[212, 212, 212],
        [211, 211, 211],
        [210, 210, 210],
        ...,
        [240, 240, 240],
        [240, 240, 240],
        [240, 240, 240]],

       [[212, 212, 212],
        [211, 211, 211],
        [210, 210, 210],
        ...,
        [240, 240, 240],
        [240, 240, 240],
        [240, 240, 240]],

       [[212, 212, 212],
        [211, 211, 211],
        [209, 209, 209],
        ...,
        [240, 240, 240],
        [240, 240, 240],
        [240, 240, 240]],

       ...,

       [[ 46,  46,  46],
        [ 45,  45,  45],
        [ 41,  41,  41],
        ...,
        [ 16,  16,  16],
        [ 12,  12,  12],
        [  6,   6,   6]],

       [[ 44,  44,  44],
        [ 47,  47,  47],
        [ 47,  47,  47],
        ...,
        [ 15,  15,  15],
        [ 12,  12,  12],
        [  5,   5,   5]],

       [[ 44,  44,  44],
        [ 49,  49,  49],
        [ 52,  52,  52],
        ...,
        [ 12,  12,  12],
        [ 10,  10,  10],
        [  4,   4,   4]]], dtype=uint8)
```

```array([[[212, 212, 212],
        [211, 211, 211],
        [210, 210, 210],
        ...,
        [240, 240, 240],
        [240, 240, 240],
        [240, 240, 240]],

       [[212, 212, 212],
        [211, 211, 211],
        [210, 210, 210],
        ...,
        [240, 240, 240],
        [240, 240, 240],
        [240, 240, 240]],

       [[212, 212, 212],
        [211, 211, 211],
        [209, 209, 209],
        ...,
        [240, 240, 240],
        [240, 240, 240],
        [240, 240, 240]],

       ...,

       [[ 46,  46,  46],
        [ 45,  45,  45],
        [ 41,  41,  41],
        ...,
        [ 16,  16,  16],
        [ 12,  12,  12],
        [  6,   6,   6]],

       [[ 44,  44,  44],
        [ 47,  47,  47],
        [ 47,  47,  47],
        ...,
        [ 15,  15,  15],
        [ 12,  12,  12],
        [  5,   5,   5]],

       [[ 44,  44,  44],
        [ 49,  49,  49],
        [ 52,  52,  52],
        ...,
        [ 12,  12,  12],
        [ 10,  10,  10],
        [  4,   4,   4]]], dtype=uint8)
```

![r02](https://github.com/user-attachments/assets/2a43d6ec-96aa-4a26-bd3b-9c6e4d8031fc)


# EX-2 EMERALD BOAT

# CODE

```
import cv2
import matplotlib.pyplot as plt

# Read the image
img = cv2.imread('bo.jpg', cv2.IMREAD_COLOR)

# Print the image shape
print("Original image shape:", img.shape)

# Convert to grayscale
gray_img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Print the grayscale image shape
print("Grayscale image shape:", gray_img.shape)

# Display the images
plt.figure(figsize=(10, 10))

plt.subplot(121)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis('off')

plt.subplot(122)
plt.imshow(gray_img, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

plt.show()
```
# OUTPUT
```
Original image shape: (500, 753, 3)
Grayscale image shape: (500, 753)
```

# ORGINAL IMAGE & GRAYSCALE IMAGE

![download](https://github.com/user-attachments/assets/ef8acb3e-d221-48b2-8ac5-10b89da141c3)



