
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
>  - Colour sensor has been set in the bottom of the EV3 so that it can recognises the colours below it.  
>  - Ultrasonic sensor has been set in the front of the EV3 so that it can recognises something in front.  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/IMG_9276.JPG" width="550px" height="350px">

### 1. Instruction of the challenge
> This chanllenge is to make LEGO EV3 to go back to the red-lined home with holding obstacle(cup).  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Collecting%20cups/image/IMG_0580.jpg" width="550px">
### 2. Algorithm
##### i) Moving all area for finding obstacles(cups)
> The movement was made to go through all areas within black line to find each cups.  
> Two cases were made to make successful movements.  
> 1. IF ROBOT FOUND CUPS  
> Go straight ➡️ Holding cup if ultrasonic sensor recognises obstacle in front ➡️ Stop movement ➡️ Go backwards until meets red line(from colour sensor) ➡️ Un-holding cup within red-lined home ➡️ Turn right some degress to go another route for finding another cup  
> 2. IF ROBOT DID NOT FIND CUPS  
> Go straight ➡️ Keep going to go until black lines(boundary line) ➡️ Stop movement ➡️ Go backwards until red line(with colour sensor) ➡️ Turn right some degrees to start to find another cups with another route    
>
> These algorithm of movements can be easily understood with figure below:  
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Collecting%20cups/image/Screen%20Shot%202020-08-04%20at%2016.07.39.png" width="450px" height="350px">  


##### ii) Holding and un-holding obstacle(cup) with ultrasonic sensor
> Ultrasonic sensor can recognises the distance from obstacles.  
> 1. IF DISTANCE OF OBSTACLES(CUP) IS LESS THAN 2CM  
> Set "holding" function to the motor of hands to turn 200 degrees.  
> 2. IF DISTANCE OF OBSTACLES(CUP) IS OVER 2CM  
> Set "do nothing" function to the motor of hands    

##### iii) Controlling colour sensor
> Colour sensor can identify each colour (red, black, white etc.)  
> 1. IF COLOUR SENSOR READ BLACK(boundary line),  
> "stop movement" and "go backwards" until red line  
> 2. IF COLOUR SENSOR READ READ(home line),  
> In the case of "Red", variable(called "front") was used to excute two cases alternately in the code:  
> + _first red meeting_ :  
> "stop movement" ➡️ move backwards a bit for putting cup within red line ➡️ un-holding cup ➡️ move backwards a bit not to hold the cup which already has been hold ➡️ turn right some degree for starting to go another route  
> + _second red meeting_ :  
> go straight even it meets red line (starting)  

### 3. How to build code
> Here is some "define"s to make whole code simple. 
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Collecting%20cups/image/defines.png" width="150px" height="250px">


### 4. Results


