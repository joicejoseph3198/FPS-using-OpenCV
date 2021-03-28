# FPS using OpenCV
 Using OpenCV for mouse control and demonstrating the use on a browser based First Person Shooter game.

 ## Working

#### Requirements:

Requirements:
Python version 3.7
pynput.mouse
Opencv2


First what we need to do is grab the live frame from our webcam and output the video on a window. This is to check if we're able to grab the frames properly without running into any trouble.

![Project Image1](https://raw.githubusercontent.com/joicejoseph3198/Images/main/1.png)

Now that that is out of the way. We need two objects that we will use to control the mouse. For example i have made use of two post-its. You can use any object as long as they have distinct color and do not clash with your background.

![Project Image1](https://raw.githubusercontent.com/joicejoseph3198/Images/main/mousecontrolfps1.png)

Next up we need to track these objects using OpenCV. For that we need to find HSV range for our objects. We use a trackbar to grab the HSV range for both the objects.

![Project Image1](https://raw.githubusercontent.com/joicejoseph3198/Images/main/2.png) 
![Project Image1](https://raw.githubusercontent.com/joicejoseph3198/Images/main/3.png)

 We will get 3 frames: named as frame, mask, and result and one mini window for Trackbars. All we need to do is keep the object in-frame and play around with the sliders of the trackbar till the object is the only thing visible and note those values. It would look something like this: 

![Project Image1](https://raw.githubusercontent.com/joicejoseph3198/Images/main/mousecontrolfps2.png)


Now the main application. We use a library called pynput.mouse to simulate the mouse control. The basic idea behind all of  this is that we create contours around the masked frame of our objects and use the coordinates of the contours to integrate it with our pynput library.


![Project Image1](https://raw.githubusercontent.com/joicejoseph3198/Images/main/4.png)

We use the orange object to move the cursor. We grab the x,y coordinates of the countour and pass them to the position() function that will move the cursor to the position of the contour. This way me can simulate the movement of the mouse.

Now to simulate left click we use the pink colored object, whenever it is in frame, it'll perform a left click. We use press(), release() function for the clicking functionality.

(Go through the Notebook in the repository to understand the code in detail. This was just a brief run through)

## Results
The working would look something like this when tested on a browser game :

![Project Image1](https://raw.githubusercontent.com/joicejoseph3198/Images/main/fpsusingopencv_VE2WiaKo_Zbrf.gif)

[Back To The Top](#read-me-template)
