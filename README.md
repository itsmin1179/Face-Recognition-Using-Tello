# Face-Recognition-Using-Tello

This project uses Tello's built-in camera drone to recognize human faces and follow them while maintaining a certain distance.

##### reference

> https://www.ryzerobotics.com/kr/tello-edu (we used this model)
>
> https://github.com/dji-sdk/Tello-Python
> 
> https://github.com/juanmapf97/Tello-Face-Recognition

The above two sites were referenced, and the second one was for Tello communication, and the third one was for applying haar-cascade.

### code execution
---

##### test.py

If you run test.py, you can control the drone with the keyboard.

> arrow up and down: change altitude
> 
> Arrow Left Right: Change the left and right angle
> 
> w s a d : front/rear/left/right


##### tello.py

You can adjust the default values of the drone. You can set the steering value (left/right) and flight altitude (up/down) at the start. Here, the flight altitude value is fixed when the program is executed using the move_up() method.

##### main.py

When you run the code, you will see a green circle in the center of the screen and three numbers in the upper left corner of the screen.

+ Green circle: The center of the camera image, which is displayed to compare the value of the distance between the center and the recognized object.
+ Three numbers: indicate the x, y, z axes of the object recognized by the camera in order.

###### Drone control according to the location of the target

> x-axis coordinates of the target (-90 < x < 90)
> 
> x  < 0 : turn left
> 
> x  > 0 : turn right
> 
> y-axis coordinates of the target (-70 < y < 70)
> 
> y  < 0 : ncrease
> 
> y  > 0 : descent
> 
> z-axis coordinates of the target (15000 < z < 30000)
> 
> z  <  15000 : move forward
> 
> z  >  30000 : move backward


#### Points to note

Since the model we used is small and light in size, it is impossible to properly control it by the wind when testing it outside, so please take this into account.



### Running video
---

[![드론영상1](https://img.youtube.com/vi/4ZNvz84VUB0/0.jpg)](https://www.youtube.com/4ZNvz84VUB0=0s) 


[![드론영상2](https://img.youtube.com/vi/_B_out6IOGs/0.jpg)](https://www.youtube.com/_B_out6IOGs=0s) 
