# [H] Attempt the following:

(a) If a five-digit number is input through the keyboard, write a program to calculate the sum of its digits. (Hint: Use the modulus operator ‘%’)

```c
#include<stdio.h>
int main(){
    int n,a,b,c,d,e,sum;
    printf("Enter 5 digit no. : ");
    scanf("%d", &n);
    a = n%10;
    n = n/10;
    b = n%10;
    n = n/10;
    c = n%10;
    n = n/10;
    d = n%10;
    n = n/10;
    e = n%10;
    sum = a+b+c+d+e;
    printf("Sum is %d", sum);
    return 0;
}
```



(b) If a five-digit number is input through the keyboard, write a program to reverse the number.

```c
#include<stdio.h>
int main(){
    int n,a,b,c,d,e,sum;
    printf("Enter 5 digit no. : ");
    scanf("%d", &n);
    a = n%10;
    n = n/10;
    b = n%10;
    n = n/10;
    c = n%10;
    n = n/10;
    d = n%10;
    n = n/10;
    e = n%10;
    sum = a*10000+b*1000+c*100+d*10+e;
    printf("Reverse is %d", sum);
    return 0;
}
```



(c) If lengths of three sides of a triangle are input through the keyboard, write a program to find the area of the triangle.

```c
#include<stdio.h>
#include<math.h>
int main(){
    float s1, s2, s3, s, area;
    printf("Enter sides of triangle : ");
    scanf("%f%f%f",&s1, &s2, &s3);
    //Heron's Formula
    s = (s1+s2+s3)/2.0;
    area = pow((s*(s-s1)*(s-s2)*(s-s3)),0.5);
    printf("Area of triangle : %f sq. units", area);
    return 0;
}
```



(d) Write a program to receive Cartesian co-ordinates (x, y) of a point and convert them into polar co-ordinates (r, ). 

Hint: r = sqrt ( x<sup>2</sup> + y<sup>2</sup> ) and tan<sup>-1</sup> ( y / x )

```c
#include<stdio.h>
#include<math.h>
int main(){
    float x, y, r, o;
    printf("Enter X and Y : ");
    scanf("%f%f", &x, &y);
    r = pow((pow(x,2)+pow(y,2)),0.5);
    o = atan(y/x);
    printf("Polar co-ordinates are : (%f, %f)", r, o);
    return 0;
}
```



(e) Write a program to receive values of latitude (L1, L2) and longitude (G1, G2), in degrees, of two places on the earth and output the distance (D) between them in nautical miles. The formula for distance in nautical miles is:

D = 3963 cos<sup>-1</sup> ( sin L1 sin L2 + cos L1 cos L2 * cos ( G2 – G1 ) )

```c
#include<stdio.h>
#include<math.h>
int main(){
    float l1, l2, g1, g2, d;
    printf("Enter L1, L2, G1, G2 : ");
    scanf("%f%f%f%f",&l1, &l2, &g1, &g2);
    d = 3963 * acos(sin(l1)*sin(l2)+cos(l1)*cos(l2)*cos(g2-g1));
    printf("Distance in nautical miles is %f", d);
    return 0;
}
```



(f) Wind chill factor is the felt air temperature on exposed skin due to wind. The wind chill temperature is always lower than the air temperature, and is calculated as per the following formula:

wcf = 35.74 + 0.6215t + ( 0.4275t - 35.75 ) * v<sup>0.16</sup>

where t is the temperature and v is the wind velocity. Write a program to receive values of t and v and calculate wind chill factor (wcf).

```c
#include<stdio.h>
#include<math.h>
int main(){
    float t,v, wcf;
    printf("Enter temperature and wind velocity : ");
    scanf("%f%f", &t, &v);
    wcf = 35.74 + 0.6215*t + ( 0.4275*t - 35.75)*pow(v,0.16);
    printf("Wind chill factor is %f", wcf);
    return 0;
}
```



(g) If value of an angle is input through the keyboard, write a program to print all its Trigonometric ratios.

```c
#include<stdio.h>
#include<math.h>
int main(){
    float a;
    printf("Enter angle : ");
    scanf("%f",&a);
    a = a/180*3.1415926535;
    printf("sin : %f\ncos : %f\ntan : %f\nsec : %f\ncosec : %f\ncot : %f",
           sin(a), cos(a), tan(a), 1/sin(a), 1/cos(a), 1/tan(a));
    return 0;
}
```



(h) Two numbers are input through the keyboard into two locations C and D. Write a program to interchange the contents of C and D.

```c
#include<stdio.h>
int main(){
    int c,d;
    printf("Enter values of C and D : ");
    scanf("%d%d",&c, &d);
    c = c+d;
    d = c-d;
    c = c-d;
    printf("Swapped values are : %d  %d", c, d);
    return 0;
}
```



(i) Consider a currency system in which there are notes of seven denominations, namely, Re. 1, Rs. 2, Rs. 5, Rs. 10, Rs. 50, Rs. 100. If a sum of Rs. N is entered through the keyboard, write a program to compute the smallest number of notes that will combine to give Rs. N.

```c
#include<stdio.h>
int main(){
    int N, r1, r2, r5, r10, r50, r100, num_of_notes;
    printf("Enter total amount : ");
    scanf("%d", &N);
    r100 = N/100;
    N = N%100;
    r50 = N/50;
    N = N%50;
    r10 = N/10;
    N = N%10;
    r5 = N/5;
    N = N%5;
    r2 = N/2;
    N = N%2;
    r1 = N;

    num_of_notes = r1+r2+r5+r10+r50+r100;
    printf("Minimum no. of notes : %d", num_of_notes);
    return 0;
}
```

