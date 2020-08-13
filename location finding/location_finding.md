

FINDING & SHOWING CURRENT LOCATION
===
Finding the location where the robot currently is
---
### Contents
>STEP 1. Ramdom location showing   
>STEP 2. Location showing of continuous movement 1 (y=x^2 graph)     
>STEP 3. Location showing of continuous movement 2 (circle)  
>4. Results  
>5. Discussions  

### STEP 1. Random location showing
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
//making random movement
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

### STEP 2. Location showing of continuous movement 1 (y=x^2 graph)  
> Making a continuous movement (not randomly as STEP1) as following y=x^2 route.  
> Building code to make continuous movement with following y=x^2 graph route.   
> Basic algorithm is :  
> making movement which follows y=x^2 graph route ➡️ show the result of location as coordinate form  
> (+ delay function was added to show the coordinate location form in visible sequence)
~~~
void delay(int number_of_seconds);
     int main (void){
         int x=0, y=0, x_o=0, y_o=0;
         while(1){
                x=x_o+x;
                x++;
                y=y_o+(x*x);
                delay(300);
                printf("the current location is (%d,%d)\n", x, y); //showing the location
         }
     }
//delay function
void delay(int number_of_seconds)
    {
    // Converting time into milli_seconds
    int milli_seconds = 1000 * number_of_seconds;
    
    // Storing start time
    clock_t start_time = clock();
    
    // looping till required time is not achieved
    while (clock() < start_time + milli_seconds);
}
~~~


### STEP3. Location showing of continuous movement 2 (circle)  
> Building code to make continuous movement (not randomly as STEP1) as making circle route.    
> Basic algorithm is :  
> making movement which follows circle route ➡️ show the result of location as coordinate form  
> (+ delay function was added to show the coordinate location form in visible sequence)  




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

