# Canny-edge-detection-workshop


## Program:
``` Python
### Developed By:Kumaran.B
### Register No:212220230026
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Load the image, Convert to grayscale and remove noise
image1=cv2.imread ('kumaran.jpg') 
gray = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)
plt.title('GRAY IMAGE')
plt.imshow(gray,cmap = 'gray')
#canny edge detection
canny_edges = cv2.Canny(gray, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.axis("off")
plt.show()
```

## Output:
![Screenshot (361)](https://user-images.githubusercontent.com/75243072/175515377-29e79f10-f55e-4f06-b239-6ca449fd0e12.png)
