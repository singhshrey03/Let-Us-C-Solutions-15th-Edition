# [F] Attempt the following:

(a) Ramesh’s basic salary is input through the keyboard. His dearness allowance is 40% of basic salary, and house rent allowance is 20% of basic salary. Write a program to calculate his gross salary.

```c
#include<stdio.h>
int main(){
    float bs, da, hra, gs;
    printf("Enter basic salary : ");
    scanf("%f", &bs);
    da = 0.4*bs;
    hra = 0.2*bs;
    gs = bs+da+hra;
    printf("Gross Salary is Rs.%f", gs);
    return 0;
}
```

(b) The distance between two cities (in km.) is input through the keyboard. Write a program to convert and print this distance in meters, feet, inches and centimeters.

```c
#include<stdio.h>
int main(){
    float km, m, ft, in, cm;
    printf("Enter distance in km  : ");
    scanf("%f", &km);
    m = 1000*km;
    ft = 3280.84*km;
    in = 12*ft;
    cm = 100*m;
    printf("%f km is %f m\n", km, m);
    printf("%f km is %f ft\n", km, ft);
    printf("%f km is %f in\n", km, in);
    printf("%f km is %f cm", km, cm);
    return 0;
}
```

(c) If the marks obtained by a student in five different subjects are input through the keyboard, write a program to find out the aggregate marks and percentage marks obtained by the student. Assume that the maximum marks that can be obtained by a student in each subject is 100.

```c
#include<stdio.h>
int main(){
    int a,b,c,d,e;
    float agg,per;
    printf("Enter marks : ");
    scanf("%d %d %d %d %d", &a, &b, &c, &d, &e);
    agg = (a+b+c+d+e)/5.0;
    printf("Aggregate Marks = %f\n", agg);
    per = (a+b+c+d+e)/ 500.0 * 100.0;
    printf("Percentage = %f %%\n",per);
    return 0;
}
```

(d) Temperature of a city in Fahrenheit degrees is input through the keyboard. Write a program to convert this temperature into Centigrade degrees.

```c
#include<stdio.h>
int main(){
    float deg_f, deg_c;
    printf("Enter temperature in Fahrenheit : ");
    scanf("%f", &deg_f);
    deg_c = (deg_f-32)*5/9;
    printf("Temperature in Centigrade is : %f", deg_c);
    return 0;
}
```

(e) The length and breadth of a rectangle and radius of a circle are input through the keyboard. Write a program to calculate the area and perimeter of the rectangle, and the area and circumference of the circle.

```c
#include<stdio.h>
int main(){
    float len, wid, rad, rec_area, rec_peri, cir_area, cir_circum;
    printf("Enter length and breadth of Rectangle & radius of Circle : ");
    scanf("%f %f %f", &len, &wid, &rad);
    rec_area = len*wid;
    rec_peri = 2*(len+wid);
    cir_area = 3.141592*rad*rad;
    cir_circum = 2*3.141592*rad;
    printf("Area of Rectangle = %f\n", rec_area);
    printf("Perimeter of Rectangle = %f\n", rec_peri);
    printf("Area of Circle = %f\n", cir_area);
    printf("Circumference of Circle = %f", cir_circum);
    return 0;
}
```

(f) Paper of size A0 has dimensions 1189 mm x 841 mm. Each subsequent size A(n) is defined as A(n-1) cut in half parallel to its shorter sides. Thus paper of size A1 would have dimensions 841 mm x 594 mm. Write a program to calculate and print paper sizes A0, A1, A2, … A8.

```c
#include<stdio.h>
int main(){
    float a0l,a0b,a1l,a1b,a2l,a2b,a3l,a3b,a4l,a4b,a5l,a5b,a6l,a6b,a7l,a7b,a8l,a8b;
    a0l = 1189;
    a0b = 841;
    a1l = a0b;
    a1b = a0l/2;
    a2l = a1b;
    a2b = a1l/2;
    a3l = a2b;
    a3b = a2l/2;
    a4l = a3b;
    a4b = a3l/2;
    a5l = a4b;
    a5b = a4l/2;
    a6l = a5b;
    a6b = a5l/2;
    a7l = a6b;
    a7b = a6l/2;
    a8l = a7b;
    a8b = a7l/2;
    printf("Dimension of A0 : %f mm x %f mm\n", a0l, a0b);
    printf("Dimension of A1 : %f mm x %f mm\n", a1l, a1b);
    printf("Dimension of A2 : %f mm x %f mm\n", a2l, a2b);
    printf("Dimension of A3 : %f mm x %f mm\n", a3l, a3b);
    printf("Dimension of A4 : %f mm x %f mm\n", a4l, a4b);
    printf("Dimension of A5 : %f mm x %f mm\n", a5l, a5b);
    printf("Dimension of A6 : %f mm x %f mm\n", a6l, a6b);
    printf("Dimension of A7 : %f mm x %f mm\n", a7l, a7b);
    printf("Dimension of A8 : %f mm x %f mm\n", a8l, a8b);
    return 0;
}
```
