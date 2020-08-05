
LEGO PROJECT - LINE FOLLOWING
===
Making LEGO EV3 to move following black line
---
### Contents
>0. Hardware
>1. Instruction of the "challenge"
>2. Algorithm
>3. How to build code
>4. Results
>5. Discussions

### 0. Hardware  
> EV3 is designed with two hands as efficient way to pull / hold something as shown below.  
> It has used three motors, two for wheels and one for holding/un-holding hands.  
> It has used two sensors, one is colour sensor and the other is ultrasonic sensor.  
>  - Colour sensor has been set in the bottom of the EV3 so that it can recognises the colours below it.  
>  - Ultrasonic sensor has been set in the front of the EV3 so that it can recognises something in front.  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/IMG_9276.JPG" width="550px" height="350px">

### 1. Instruction of the challenge
> This chanllenge is to make LEGO EV3 to move following black line with using colour sensor.
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/IMG_0294.JPG" width="550px">
### 2. Algorithm
##### i) Moving left and right as following black lines
> Basically, the movement of the EV3 is made as :  
> Move left and right around the black line based on the data(reflected light) from the colour sensor.  
> Go right side if intensity of reflected light is less than some extent ➡️ Go left side if intensity of reflected light is more than some extent ...(repeat)

##### ii) Get data(reflected light) from colour sensor
> Measure the extent of reflected light to see which variable of reflected light intensity can be used for deciding to turn right or left.
> The reflected light intensity can be shown in the screen of EV3 Classroom.
> Image below shows that how intensity of reflected light can be measured.  
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/Screen%20Shot%202020-08-04%20at%2013.16.18.png" width="650px" height="100px">  
> _colour sensor is connected to 3, ultrasonic sensor is connected to 4, and two motors are connected to A and B (D is for controlling hands)_

### 3. How to build code
> The code can be built as two ways :
> One is making on brick program in the EV3 robot. It is the way to put code directly in the EV3.  
> Brick program can be built as shown below.  
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/IMG_0249.JPG" width="350px" height="250px">
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/IMG_0250.JPG" width="350px" height="250px">
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/IMG_0251.JPG" width="350px" height="250px">
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/IMG_0252.JPG" width="350px" height="250px">  
> The other way is making code in the EV3 Classroom.  
> This code is shown below.  
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/Screen%20Shot%202020-08-04%20at%2013.15.46.png" width="650px" height="350px">  

### 4. Results
> The EV3 robot could follow black line successfully.  
> However, it does not naturally follow the black line because the code is made as kind of digital logic(0 and 1).  
> In other words, turn left(0) when intensity of reflected light is less than some extent  
> and turn right (1) when intensity of reflected light is more than some extent. (more likely to call "bang-bang control")  
> So robot can control the direction to follow the black line. 
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/animated.GIF" width="650px" height="350px">  
> _short version of line following_  
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/animated 2.GIF" width="650px" height="350px">  
> _full version of line following_  

### 5. Discussions  
> Since the code is made like bang-bang control, the robot does not follow black line naturally.  
> Bang-bang control is a feedback controller which switches abruptly between two states, with realising any element that provides hysteresis. 
> How to solve ?  
> Using PID controller to make follwing smoothly.  
> Implementing/ Installing(?) high quality sensors to identify black line exactly.
