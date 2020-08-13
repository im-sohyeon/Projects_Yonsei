

FINDING & SHOWING CURRENT LOCATION
===
Finding the location where the robot currently is
---
### Contents
>STEP 1. Ramdom location showing   
>STEP 2. Location showing of continuous movement 1 (y=x^2 graph)     
>STEP 3. Location showing of continuous movement 2 (circle)  
>STEP 4. Results  
>5. Discussions  

### STEP 1. Random location showing
> Building a code to make random movement and stop movement with showing the result of location when "2" is pressed.  
> Basic algorithm is :  
> move ramdomly ➡️ stop moving if "2"is pressed ➡️ show the result of location as coordinate form  
~~~
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <math.h>

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
> (+ delay function was added to show the coordinates of location in visible sequence)
~~~
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <math.h>

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
> making movement which follows circle route(radius=5) ➡️ show the result of location as coordinate form  
> (+ delay function was added to show the coordinates of location in visible sequence)  
> To make movement of circle, angle(represents as thetha in the code) which converts to radians is used as an increment factor in for loop.   
~~~
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <math.h>

void delay(int number_of_seconds);
double DegreesToRadians( double degrees );
#define PI 3.141592
     int main (void){
         double x=0.0, y=0.0, x_o=0.0, y_o=0.0, thetha=0.0, radians=0.0;
         while(1){
             for(thetha=0.0;thetha<360;thetha++){
                 double radians = DegreesToRadians( thetha );
                 x=5*cos(radians);
                 y=5*sin(radians);
                 delay(50);
                 printf("thetha = %lf\n",thetha);
                 printf("the current location is (%lf,%lf)\n", x, y); //showing the location
             }
         }
     }
//degrees to radians 
double DegreesToRadians( double degrees )
{
    return degrees * PI / 180;
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



### STEP 4. Giving specific condition 


### 4. Results
> 

### 5. Discussions
> Problem:   
> Since real movement of robot(as shown in results) is not as same as ideal movement which mentioned in Algorithm of movement,  
> it sometimes could happen that robot could not include all cups in its route. 
>  
> How to solve this problem?  
> 1. Check the performance of two different motors,  
> 2. And try to make ideal movement with many attempts to match movement algorithm  

