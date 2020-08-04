
LEGO PROJECT - COLLECTING CUPS WITHIN RED-LINED HOME
===
Making LEGO EV3 to collect/hold each cups and back to the red-lined home
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
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/IMG_9276.JPG" width="550px" height="350px">

### 1. Instruction of the challenge
> This chanllenge is to make LEGO EV3 to go back to the red-lined home with holding obstacle(cup).  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Collecting%20cups/image/IMG_0580.jpg" width="550px">
### 2. Algorithm
##### i) Moving all area for finding obstacles(cups)
> The movement was made to go through all areas within black line to find each cups.  
> There are two cases in making movements.  
> 1. IF ROBOT FOUND CUPS  
> Go straight ➡️ Holding cup if ultrasonic sensor recognises obstacle in front ➡️ Go backwards until meets red line(from colour sensor) ➡️ Un-holding cup within red-lined home ➡️ Turn right some degress to go another routes for finding another cup  
> 2. IF ROBOT DID NOT FIND CUPS  
> Go straight ➡️ Keep going to go until black lines ➡️ Stop movement ➡️ Go backwards until red line ➡️ Turn right some degrees to start to find another cups with another routes    
> This algorithm of movement can be easily understood with figure below:  
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/Screen%20Shot%202020-08-04%20at%2013.16.18.png" width="650px" height="100px">  


##### ii) Holding and un-holding obstacle(cup) with ultrasonic sensor
> Measure the extent of reflected light to see which variable of reflected light intensity can be used for deciding to turn right or left.
> The reflected light intensity can be shown in the screen of EV3 Classroom.
> Image below shows that how intensity of reflected light can be measured.  
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/line%20following/image/Screen%20Shot%202020-08-04%20at%2013.16.18.png" width="650px" height="100px">  
> _colour sensor is connected to 3, ultrasonic sensor is connected to 4, and two motors are connected to A and B (D is for controlling hands)_

##### iii) Holding obstacle(cup) from ultrasonic sensor

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


