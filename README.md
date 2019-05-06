# VisualRepresentationSotApp

This Repository contains Application code for 200 elements with delay to represent accurately and also 1000 elements sorting without delay.
Application Code:

This is a C++ Application to visualize the Bubble.
with the same method we can create application for other sorting algorithms.

Pre-requisites:
1. Dev C++
2. enable graphics in Dev C++ 
    see how to enable graphics in dev c++ here: https://www.youtube.com/watch?v=TEMhWt9WwTA
    
Now You good to write your graphics code:

We will see the code in two parts :
1. whole code
2. step by step description of the code

Code:
// code Starts from here................................................................................................................


//Visual Represtation of Bubble Sort.


#include <iostream>
#include <graphics.h>
#include <conio.h>
#include <dos.h>
using namespace std;


// bubbleSort Function Definition that sorts the elements

void bubbleSort(int a[],int a1[],int a2[]){


	for(int j=0;j<199;j++)
	{
		int done=0;
		for(int k=0;k<(200-j)-1;k++){
			if(a[k]>a[k+1])
			{
				setcolor(0);
				line(a1[k],a[k],a2[k],550);
				line(a1[k+1],a[k+1],a2[k+1],550);
				swap(a[k],a[k+1]);
				setcolor(3);
				line(a1[k],a[k],a2[k],550);
				line(a1[k+1],a[k+1],a2[k+1],550);
				done=1;
				//delay(1);
					
			}
			
	    }
	    
	    if(done==0){
	    	
	    	break;
		}
	}
	
	 outtextxy(450,30, "Processing Done to Sort" );
}

  // main function
  
  
int main()
{
   int gd = DETECT, gm;
   int i,x1=100,y1,x2=100;
   int array[200];
   int array1[200],array2[200];
 
   initgraph(&gd, &gm, "C:\\TC\\BGI");
   
   outtextxy(450,10, "Bubble Sort Visual Reprentation" );
   delay(2000);
 //Unsorted Elements
 
 for(i=0;i<200;i++)
 {
 	x1=100,x2=100;
 	y1=(rand()%(500-50+1))+50;
	 
	x1=x1+5*i;
 	x2=x2+5*i;
 	line(x1, y1, x2, 550);
 	array[i]=y1;
 	array1[i]=x1;
 	array2[i]=x2;
 	
 	delay(20);
 }
 
 // calling of bubbleSort function to sort the elements
 
    delay(2000);
    bubbleSort(array,array1,array2);
    getch();
    closegraph();
	return 0;
}

// Code finishes here...................................................................................................................


Code Description:

1. Creation of Unsorted Lines:

//Unsorted Elements
 
 for(i=0;i<200;i++)
 {
 	x1=100,x2=100;
 	y1=(rand()%(500-50+1))+50;
	 
	x1=x1+5*i;
 	x2=x2+5*i;
 	line(x1, y1, x2, 550);
 	array[i]=y1;
 	array1[i]=x1;
 	array2[i]=x2;
 	
 	delay(20);
 }
 
 We have created random height lines. where height is represted by the y1 variable.
 Random numbers are generated for y1's values. 
 Limitation/Range is given to the y1 variable to make the height of the variable inside our window.
 
 y1=(rand()%(500-50+1))+50;
 
 the perameters x1, x2, y1 are saved in different unique arrays, so that can be used later in the programme.
 a delay of 20ms is provided so that visualization can be more accurate.
 
 2. sorting the unsorted lines:
 
 // Sorting Function:
 
 void bubbleSort(int a[],int a1[],int a2[]){


	for(int j=0;j<199;j++)
	{
		int done=0;
		for(int k=0;k<(200-j)-1;k++){
			if(a[k]>a[k+1])
			{
				setcolor(0);
				line(a1[k],a[k],a2[k],550);
				line(a1[k+1],a[k+1],a2[k+1],550);
				swap(a[k],a[k+1]);
				setcolor(3);
				line(a1[k],a[k],a2[k],550);
				line(a1[k+1],a[k+1],a2[k+1],550);
				done=1;
				//delay(1);
					
			}
			
	    }
	    
	    if(done==0){
	    	
	    	break;
		}
	}
	
	 outtextxy(450,30, "Processing Done to Sort" );
}

.............

The function takes the 3 perameters array1,array2 and array corresponds to x1, x2, and y1 as arguments.
further code is same as we do the bubble sort in c++ programming.
the logic here of sorting is : 

only one perameter that y1 is being sort and after comparision of y1 elements they swap if they fulfil the condition.

You can see the output gif and video aploaded in the repository to understand it better.
.............

Happy Coding...................
Rakhi Soni
 
