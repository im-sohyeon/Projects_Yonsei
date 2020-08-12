

FINDING & SHOWING CURRENT LOCATION
===
Finding the location where the robot currently is
---
### Contents
>STEP 1. Ramdom location showing   
>STEP 2. location showing of continuous moving   
>3. How to build code  
>4. Results  
>5. Discussions  

### STEP1. Random location showing
> Building a code to make random movement and stop movement with showing the result of location when "2" is pressed.  
> Basic algorithm is :
> move ramdomly ➡️ stop moving if "2"is pressed ➡️ show the result of location as coordinate form  
~~~
void randommove(int Row, int Column, int *rowplus, int *columnplus) ;

 int main (void){
     int i=0;
     int Row = 0, Column = 0,rowplus,columnplus;

     printf("Push 2 to stop movement: \n");
    
     while (i != 2)
     {
         scanf("%d",&i);
         randommove(Row,Column,&rowplus,&columnplus);
         Row=rowplus;
         Column=columnplus;
         printf("the current location is (%d,%d)\n", Row, Column);
         printf("number %d is pushed, so the movement is stopped\n" ,i);
     }
}
//making random moving
void randommove(int Row, int Column, int *rowplus, int *columnplus) {
    srand((unsigned int)time(NULL));
    int direction= rand() %8+ 0;
    Column = rand() % 8 +1;
    Row = rand() % 8 + 1;
    switch(direction){
        case 0: // East
            *rowplus=Row+1; *columnplus=Column;
            break;
        case 1: // North East
            *rowplus=Row+1; *columnplus=Column-1;
            break;
        case 2: // North
            *rowplus=Row; *columnplus=Column-1;
            break;
        case 3: // North West
            *rowplus=Row-1; *columnplus=Column-1;
            break;
        case 4: // West
            *rowplus=Row-1; *columnplus=Column;
            break;
        case 5: // South West
            *rowplus=Row-1; *columnplus=Column+1;
            break;
        case 6: // South
            *rowplus=Row; *columnplus=Column+1;
            break;
        case 7: // South East
            *rowplus=Row+1; *columnplus=Column+1;
            break;
    }
}
~~~

### STEP 2. location showing of continuous moving  
> Making a continuous movement (not randomly as STEP1) as following y=x route.  
> Building code to make continuous movement with following y=x graph route.   
> Basic algorithm is :
> movement, following y=x graph route ➡️ stop moving if "enter"is pressed ➡️ show the result of location as coordinate form when it stops    
>


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

