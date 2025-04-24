## EX 1: DDA ALGORITHM 

**Aim :**

To  implement the DDA algorithm to draw a line using a c coding

**Algorithms :**

Step 1 − Get the input of two end points (X0,Y0) and (X1,Y1)

Step 2 − Calculate the difference between two end points dx and  dy 

Step 3 − If dx > dy, then you need more steps in x coordinate; otherwise in y coordinate.

Step 4 − Calculate the increment in x coordinate and y coordinate

Step 5 − Plot the pixel by successfully incrementing x and y coordinates accordingly and complete the drawing of the line

**Program :**

#include "stdio.h"
#include "conio.h"
#include "math.h"
#include "graphics.h"
main()
{
int gd=DETECT,gm;
int xa,xb,ya,yb;
int dx,dy,x,y,xend,p;
initgraph(&gd,&gm,"c:\\tc\\bgi");
printf("Enter The Two Left Endpoints(xa,ya):\n");
scanf("%d%d",&xa,&ya);
printf("Enter The Two Right Endpoints(xb,yb):\n");
scanf("%d%d",&xb,&yb);
dx=abs(xa-xb);
dy=abs(ya-yb);
p=2*dy-dx;
if(xa>xb)
{
x=xb;
y=yb;
xend=xa;
}
else
{
x=xa;
y=ya;
xend=xb;
}
 putpixel(x,y,6);
 while(x<xend)
 {
 x=x+1;
 if(p<0)
 {
 p=p+2*dy;
 }
 else
 {
 y=y+1;
 p=p+2*(dy-dx);
 }
 putpixel(x,y,6);
 }
 getch();
 return(0);
}

**Output :**
Register No: 212224230009
Name: AHAMADH SULAIMAN M
![Screenshot 2025-04-23 103856](https://github.com/user-attachments/assets/7f9e8f0c-5b4e-4a42-b130-6d54754ec907)


**Result :**
Result : The DDA algorithm to draw a line using a c coding is sucessfully verified.
