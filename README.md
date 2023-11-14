# Image-Acquisition-from-Web-Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
<br>
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
 Import the cv2 and numpy package.
<br>

### Step 2:
Read the Video frame using the cv2.VideoCapture(0)
<br>

### Step 3:
Write the image using imwrite().
<br>

### Step 4:
Display the frame using the imshow().
<br>

### Step 5:
Divide the frame into halves and assign the smaller frame
<br>
### Step 6:
Rotate the frame using the cv2.rotate().
<br>

## Program:

### Developed By:ROSHINI RK
### Register No:212222230123

## i) Write the frame as JPG file
``` Python
import cv2
obj = cv2.VideoCapture(0)
while(True):
    cap,frame = obj.read()
    cv2.imshow('video.jpg',frame)
    cv2.imwrite("purse.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
obj.release()
```
## ii) Display the video
``` Python
import cv2
img = cv2.VideoCapture(0)
while(True):
    imagee,frame = img.read()
    cv2.imshow('ROSHINI RK',frame)
    cv2.imwrite("NewPicture.jpg",frame)
    if cv2.waitKey(1) == ord('q'):
        break
img.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
``` Python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('ROSHINI R K 212222230123',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iv) Rotate and display the video
``` Python
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)
    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2] = smaller_frame 
    image[:height//2, width//2:] = smaller_frame
    image[height//2:, width//2:] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    cv2.imshow('ROSHINI R K 212222230123', image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```
## Output

### i) Write the frame as JPG image

![image](https://github.com/roshiniRK/Image-Acquisition-from-Web-Cameraa/assets/118956165/faf4cca9-cf90-4e2b-a0bb-23c62dbd06f7)



### ii) Display the video

![image](https://github.com/roshiniRK/Image-Acquisition-from-Web-Cameraa/assets/118956165/0f10bd5b-48aa-4cef-af3b-098254879737)


### iii) Display the video by resizing the window


![image](https://github.com/roshiniRK/Image-Acquisition-from-Web-Cameraa/assets/118956165/6cb9e17f-bf68-48ea-9a06-9b9f299eb9d4)



### iv) Rotate and display the video


![image](https://github.com/roshiniRK/Image-Acquisition-from-Web-Cameraa/assets/118956165/79ff9c35-d2ea-4f04-ba96-382b5281e764)



## Result:
Thus the image is accessed from webcamera and displayed using openCV.
