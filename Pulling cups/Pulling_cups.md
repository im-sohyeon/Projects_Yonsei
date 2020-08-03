
LEGO PROJECT - PULLING CUPS
===
Making LEGO EV3 to pull cups over black square lines
---
### Contents
>1. Instruction of the "challenge"
>2. Algorithm
>3. How to build code
>4. Results
>5. What do i learn?
### 1. Instruction of the challenge
> This chanllenge is to make LEGO EV3 to pull cups which is located randomly to the out of black square lines as shown below.  
>
> <img src = "https://github.com/im-sohyeon/Projects_Yonsei/blob/master/Pulling%20cups/image/IMG_0577.jpg" width="550px">
### 2. Algorithm
##### i) Moving within the black lines
> Basically, the movement of the EV3 is made as :  
> Go straight until meet black line ➡️ Turn back (right side) ➡️ Go straight until meet black line  ➡️ Turn back (left side) ...(repeat)

##### ii) Holding cups
> For pulling cups, it is no need to hold each cups one by one for making possibility higher ~~~~~
For this, hands of EV3 is set as "open state" all the time to pull all cups which is located in same line.\

##### iii) Pulling cups over black lines
> Make EV3 to move until black lines by using colour sensor.
> If colour sensor recognises the black line, EV3 stops to move
> so that cups, which is inside of EV3's hand, can be located out of the black line.
