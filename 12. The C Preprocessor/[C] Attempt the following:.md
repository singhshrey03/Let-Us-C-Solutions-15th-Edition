# [C] Attempt the following:

(a) If a macro is not getting expanded as per your expectation, how will you find out how is it being expanded by the preprocessor.

````
By getting the expanded source code (intermediate code) using the command:
gcc -E test.C > test.I
````

(b) Write down macro definitions for the following:

1. To test whether a character is a small case letter or not.

   ````c
   #define ISSMALL(x) (x >= 97 && x <= 122 ? 1 : 0)
   ````

2. To test whether a character is a upper case letter or not.

   ````c
   #define ISUPPER(y) (y >= 65 && y <= 90 ? 1 : 0)
   ````

3. To test whether a character is an alphabet or not. Make use of the macros you defined in 1 and 2 above.

   ````c
   #define ISALPHA(z) (ISSMALL(z) || ISUPPER(z))
   ````

4. To obtain the bigger of two numbers.

   ````c
   #define BIGGER(a,b) (a > b ? a : b)
   ````

(c) Write macro definitions with arguments for calculation of area and perimeter of a triangle, a square and a circle. Store these macro definitions in a file called “areaperi.h”. Include this file in your program, and call the macro definitions for calculating area and perimeter for different squares, triangles and circles.

````c
//areaperi.h

#define AREAT(b,h) (0.5*b*h)
#define PERIT(x,y,z) (x+y+z)
#define AREAS(s) (s*s)
#define PERIS(s) (4*s)
#define PI 3.141592
#define AREAC(r) (PI*r*r)
#define PERIC(r) (2*PI*r)
````

````c
//areaperi.c

#include "areaperi.h"
#include<stdio.h>
int main()
{
    int b,h,x,y,z,s,r;
    float areat,perit,areas,peris,areac,peric;

    printf("Enter base and height of triangle: ");
    scanf("%d%d", &b, &h);
    areat = AREAT(b,h);
    printf("Area of triangle = %f\n",areat);

    printf("Enter 3 sides of triangle: ");
    scanf("%d%d%d",&x, &y, &z);
    perit = PERIT(x,y,z);
    printf("Perimeter of triangle = %f\n",perit);

    printf("Enter side of square: ");
    scanf("%d", &s);
    areas = AREAS(s);
    printf("Area of square = %f\n",areas);
    peris = PERIS(s);
    printf("Perimeter of square = %f\n",peris);

    printf("Enter radius of circle: ");
    scanf("%d", &r);
    areac = AREAC(r);
    printf("Area of circle = %f\n",areac);
    peric = PERIC(r);
    printf("Circumference of circle = %f\n",peric);

    return 0;
}
````

(d) Write down macro definitions for the following:

1. To find arithmetic mean of two numbers.

   ````c
   #define AMEAN(a,b) ((a + b) / 2)
   ````

2. To find absolute value of a number.

   ````c
   #define ABSOLUTE(x) (x < 0 ? x*-1 : x)
   ````

3. To convert a upper case alphabet to lower case.

   ````c
   #define UPTOLOW(y) (y + 32)
   ````

4. To obtain the bigger of two numbers.

   ````c
   #define BIGGER(x,y,z) (x>y && x>z ? x : (y>x && y>z ? y : z))
   ````

(e) Write macro definitions with arguments for calculation of Simple Interest and Amount. Store these macro definitions in a file called “interest.h”. Include this file in your program, and use the macro definitions for calculating simple interest and amount.

````c
//interest.h

#define SI(p,n,r) (p*n*r/100)
#define AMT(p,SI) (p+SI)
````

````c
//interest.c

#include "interest.h"
#include<stdio.h>
int main(){
    int p, n, r;
    float si, amt;
    printf("Enter values of p, n and r: ");
    scanf("%d%d%d",&p,&n,&r);
    si = SI(p,n,r);
    printf("Simple Interest = %f\n",si);
    amt = AMT(p,SI(p,n,r));
    printf("Amount = %f\n",amt);
    return 0;
}
````

