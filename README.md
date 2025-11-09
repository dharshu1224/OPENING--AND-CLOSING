# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

# Step1:
Import the necessary packages.

# Step2:
Create the Text using cv2.putText.

# Step3:
Create the structuring element.

# Step4:
Use Opening operation.

# Step5:
Use Closing Operation.

 
## Program:

# Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'JANARTHANAN K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```

# Create the structuring element

```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11))

```

# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")
```

# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```












## Output:

### Display the input Image

<img width="801" height="201" alt="image" src="https://github.com/user-attachments/assets/90215338-3a44-422a-b5a0-162c71d92396" />


### Display the result of Opening

<img width="833" height="191" alt="image" src="https://github.com/user-attachments/assets/7f9f0a1d-5ed3-42db-9b30-917f282853bc" />


### Display the result of Closing

<img width="825" height="208" alt="image" src="https://github.com/user-attachments/assets/bfcb70ab-2902-43ce-bb6f-b12a765923d4" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
