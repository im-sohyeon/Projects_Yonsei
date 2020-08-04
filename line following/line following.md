
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
>5. What do i learn?
### 0. Hardware  
> EV3 is designed with two hands as efficient way to pull / hold something as shown below.  
> It has used three motors, two for wheels and one for holding/un-holding hands.  
> It has used two sensors, one is colour sensor and the other is ultrasonic sensor.  
>  - Colour sensor is set in the bottom of the EV3 so that it can recognises the colours below it.  
>  - Ultrasonic sensor is set in the front of the EV3 so that it can recognises something in front.  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/IMG_9276.JPG" width="550px" height="400px">

### 1. Instruction of the challenge
> This chanllenge is to make LEGO EV3 to move following black line with using colour sensor
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/IMG_0294.JPG" width="550px">
### 2. Algorithm
##### i) Moving left and right as following black lines
> Basically, the movement of the EV3 is made as :  
> Move left and right around the black line based on the data(reflected light) from the colour sensor
> Go right side if reflected light is less than some extent ➡️ Go left side if reflected light is more than some extent ...(repeat)

##### ii) Get data(reflected light) from colour sensor
> Measure the extent of reflected light to see which variable of reflected light intensity can be used for deciding to turn right or left.
> The reflected light intensity can be shown in the screen of EV3 Classroom.

### 3. How to build code
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/Screen%20Shot%202020-07-28%20at%2010.00.07.png" width="550px" height="450px">
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/Screen%20Shot%202020-07-28%20at%2010.00.24.png" width="550px" height="550px">

### 4. Results

