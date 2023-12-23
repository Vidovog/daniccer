# daniccer
Servis game
# Code for Image Processing with OpenCV
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Load an image from file
image_path = 'path/to/your/image.jpg'
image = cv2.imread(image_path)

# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

# Apply a Gaussian blur
blurred_image = cv2.GaussianBlur(gray_image, (5, 5), 0)

# Display the original and processed images side by side
plt.subplot(1, 2, 1), plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)), plt.title('Original Image')
plt.subplot(1, 2, 2), plt.imshow(blurred_image, cmap='gray'), plt.title('Blurred Image')
plt.show()
