# OPENING--AND-CLOSING
## Name: Lakshmen Prashanth R 
## Reg.No: 212224230137
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Create the Text using cv2.putText
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'LAKSHMEN PRASHANTH ', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Create the structuring element
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Use Opening operation
# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')

# Use Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closed_image)
plt.axis("off")
```
## Output:

### Display the input Image
<img width="836" height="549" alt="Screenshot 2025-11-12 111537" src="https://github.com/user-attachments/assets/431b8b7b-d4e2-409f-9251-891e8aea49c2" />



### Display the result of Opening
<img width="836" height="549" alt="Screenshot 2025-11-12 111537" src="https://github.com/user-attachments/assets/daee9718-65c4-40e5-8b0b-b2711cd869e6" />



### Display the result of Closing
<img width="836" height="549" alt="Screenshot 2025-11-12 111537" src="https://github.com/user-attachments/assets/e20c715c-bded-4555-a04f-29d8934e551e" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
