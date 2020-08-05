
LEGO PROJECT - PULLING CUPS
===
Making LEGO EV3 to pull cups over black square lines
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
>  - Ultrasonic sensor has been set in the front of the EV3 so that it can figure out obstacles in front.  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/IMG_9276.JPG" width="550px" height="400px">

### 1. Instruction of the challenge
> This chanllenge is to make LEGO EV3 to pull cups which is located randomly to the out of black square lines as shown below.  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/IMG_0577.jpg" width="550px">
### 2. Algorithm
##### i) Moving within the black lines
> Basically, the movement of the EV3 is made as :  
> Go straight until meet black line ➡️ Turn back (right side) ➡️ Go straight until meet black line  ➡️ Turn back (left side) ...(repeat)   
> This algorithm of movement is shown below :  
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/movement.png" width="450px">


##### ii) Holding cups
> It is no need to hold each cups one by one in this challenge for making high possibility in catching all cups in a same line.
For this, hands of EV3 is set as "open state" all the time.

##### iii) Pulling cups over black lines
> Make EV3 to move until black lines by using colour sensor.
> If colour sensor recognises the black line, EV3 stops to move
> so that cups, which is inside of EV3's hand, can be located out of the black line.

### 3. How to build code
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/pulling_code.png" width="450px" height="650px">


### 4. Results
> There are two results of challenge called pulling cups.  
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/pullingcup.GIF" width="550px" height="350px">  
>_result 1 of pulling cups_  
><img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/pullingcup2.GIF" width="550px" height="350px">  
>_result 2 of pulling cups_

### 5. Discussions
> Problem:   
> Since real movement of robot(as shown in results) is not as same as ideal movement which mentioned in Algorithm of movement,  
> it sometimes could happen that robot could not include all cups in its route. 
>  
> How to solve this problem?  
> 1. Check the performance of two different motors,  
> 2. And try to make ideal movement with many attempts to match movement algorithm  

