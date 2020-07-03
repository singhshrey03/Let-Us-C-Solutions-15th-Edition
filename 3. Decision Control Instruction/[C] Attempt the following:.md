# [C] Attempt the following:

(a) If cost price and selling price of an item are input through the keyboard, write a program to determine whether the seller has made profit or incurred loss. Also determine how much profit he made or loss he incurred.

````c
#include<stdio.h>
int main(){
    int cp, sp;
    printf("Enter Cost Price and Selling Price : ");
    scanf("%d%d", &cp, &sp);
    if(sp - cp > 0){
        printf("Profit is Rs.%d", sp - cp);
    }
    else if(sp - cp < 0){
        printf("Loss is Rs.%d",cp - sp);
    }
    else{
        printf("No Profit No Loss");
    }
    return 0;
}
````



(b) Any integer is input through the keyboard. Write a program to find out whether it is an odd number or even number.

````c
#include<stdio.h>
int main(){
    int n;
    printf("Enter a no. : ");
    scanf("%d", &n);
    if(n % 2 == 0){
        printf("EVEN");
    }
    else{
        printf("ODD");
    }
    return 0;
}
````



(c) Any year is input through the keyboard. Write a program to determine whether the year is a leap year or not.

(Hint: Use the % (modulus) operator)

````c
#include<stdio.h>
int main(){
    int year;
    printf("Enter year : ");
    scanf("%d", &year);
    if(year % 4 == 0){
        if(year % 100 != 0){
            printf("Leap Year");
        }
        else if(year % 400 == 0){
            printf("Leap Year");
        }
        else{
            printf("Not a Leap Year");
        }
    }
    else{
        printf("Not a Leap Year");
    }
    return 0;
}
````



(d) According to the Gregorian calendar, it was Monday on the date 01/01/01. If any year is input through the keyboard write a program to find out what is the day on 1st January of this year.

````c
#include<stdio.h>
int main(){
    int day, total_days, input_year, leap_year, normal_year, difference;
    int reference_year = 2001;
    printf("Enter a year : ");
    scanf("%d", &input_year);
    difference = abs(input_year - reference_year);
    leap_year = difference / 4;
    normal_year = difference - leap_year;
    total_days = (normal_year * 365) + (leap_year * 366);
    day = total_days % 7;
    if(day == 0){
        printf("Monday");
    }
    else if(day == 1){
        printf("Tuesday");
    }
    else if(day == 2){
        printf("Wednesday");
    }
    else if(day == 3){
        printf("Thursday");
    }
    else if(day == 4){
        printf("Friday");
    }
    else if(day == 5){
        printf("Saturday");
    }
    else if(day == 6){
        printf("Sunday");
    }
    return 0;
}
````



(e) A five-digit number is entered through the keyboard. Write a program to obtain the reversed number and to determine whether the original and reversed numbers are equal or not.

````c
#include<stdio.h>
int main(){
    int n,a,b,c,d,e,sum,num;
    printf("Enter 5 digit no. : ");
    scanf("%d", &n);
    num = n;
    a = n % 10;
    n = n / 10;
    b = n % 10;
    n = n / 10;
    c = n % 10;
    n = n / 10;
    d = n % 10;
    n = n / 10;
    e = n % 10;
    sum = a * 10000 + b * 1000 + c * 100 + d * 10 + e;
    if(num == sum){
        printf("Reverse is same");
    }
    else{
        printf("Reverse is not same");
    }
    return 0;
}
````



(f) If the ages of Ram, Shyam and Ajay are input through the keyboard, write a program to determine the youngest of the three.

````c
#include<stdio.h>
int main(){
    int ram, shyam, ajay;
    printf("Enter ages of Ram, Shyam and Ajay : ");
    scanf("%d%d%d", &ram, &shyam, &ajay);
    if(ram < shyam && ram < ajay){
        printf("Ram is youngest");
    }
    else if(shyam < ram && shyam < ajay){
        printf("Shyam is youngest");
    }
    else{
        printf("Ajay is youngest");
    }
return 0;
}
````



(g) Write a program to check whether a triangle is valid or not, when the three angles of the triangle are entered through the keyboard. A triangle is valid if the sum of all the three angles is equal to 180 degrees.

````c
#include<stdio.h>
int main(){
    int a, b, c;
    printf("Enter angles of Triangle : ");
    scanf("%d%d%d", &a, &b, &c);
    if(a + b + c == 180){
        printf("Valid");
    }
    else{
        printf("Invalid");
    }
    return 0;
}
````



(h) Write a program to find the absolute value of a number entered through the keyboard.

````c
#include<stdio.h>
#include<math.h>
int main(){
    int n;
    printf("Enter a  no. : ");
    scanf("%d", &n);
    printf("Absolute value is %d", abs(n));
    return 0;
}
````



(i) Given the length and breadth of a rectangle, write a program to find whether the area of the rectangle is greater than its perimeter. For example, the area of the rectangle with length = 5 and breadth = 4 is greater than its perimeter.

````c
#include<stdio.h>
int main(){
    int length, breadth, area, perimeter;
    printf("Enter Length and Breadth : ");
    scanf("%d%d", &length, &breadth);
    area = length * breadth;
    perimeter = 2*(length + breadth);
    if(area > perimeter){
        printf("Area is greater");
    }
    else{
        printf("Perimeter is greater");
    }
    return 0;
}
````



(j) Given three points **(x1, y1)**, **(x2, y2)** and **(x3, y3)**, write a program to check if all the three points fall on one straight line.

````c
#include<stdio.h>
int main(){
    int x1, x2, x3, y1, y2, y3;
    printf("Enter point 1 : ");
    scanf("%d%d", &x1, &y1);
    printf("Enter point 2 : ");
    scanf("%d%d", &x2, &y2);
    printf("Enter point 3 : ");
    scanf("%d%d", &x3, &y3);
    if((x1*(y2-y3) - x2*(y1-y3) + x3*(y1-y2)) == 0){
        printf("YES. The above points are collinear\n");
    }
    else{
        printf("NO. The above points are NOT collinear\n");
    }
    return 0;
}
````



(k) Given the coordinates **(x, y)** of center of a circle and its radius, write a program that will determine whether a point lies inside the circle, on the circle or outside the circle. (Hint: Use **sqrt( )** and **pow( )**
functions)

````c
#include<stdio.h>
#include<math.h>
int main(){
    int x, y, rad, a, b;
    float dist;
    printf("Enter center of Circle : ");
    scanf("%d%d", &x, &y);
    printf("Enter radius : ");
    scanf("%d", &rad);
    printf("Enter the new point : ");
    scanf("%d%d", &a, &b);
    dist = pow( (pow((x-a), 2) + pow((y-b), 2)), 0.5);
    if(dist > rad){
        printf("Outside");
    }
    else if(dist < rad){
        printf("Inside");
    }
    else{
        printf("On");
    }
    return 0;
}
````



(l) Given a point **(x, y)**, write a program to find out if it lies on the X-axis, Y-axis or on the origin.

````c
#include<stdio.h>
int main(){
    int x,y;
    printf("Enter the point : ");
    scanf("%d%d",&x,&y);
    if(x == 0 && y == 0){
        printf("Origin");
    }
    else if(x == 0 && y != 0){
        printf("Y-axis");
    }
    else if(x != 0 && y == 0){
        printf("X-axis");
    }
    else{
        printf("Not on any axis");
    }
    return 0;
}
````

