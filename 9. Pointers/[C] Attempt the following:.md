# [C] Attempt the following:

(a) Write a function that receives 5 integers and returns the sum, average and standard deviation of these numbers. Call this function from **main( )** and print the results in **main( )**.

````c
#include<stdio.h>
#include<math.h>
void sum_avg_std(int, int, int, int, int, float *, float *, float *);
int main(){
    int a, b, c, d, e;
    float sum, avg, std;
    printf("Enter 5 numbers: ");
    scanf("%d%d%d%d%d", &a, &b, &c, &d, &e);
    sum_avg_std(a, b, c, d, e, &sum, &avg, &std);
    printf("Sum = %f\nAverge = %f\nStandard Deviation = %f\n",sum, avg, std);
    return 0;
}
void sum_avg_std(int i,int j, int k, int l, int m, float *s, float *a, float *d){
    *s = i + j + k + l + m;
    *a = *s / 5.0;
    *d = sqrt((pow(i-*a, 2)+pow(j-*a, 2)+pow(k-*a, 2)+pow(l-*a, 2)+pow(m-*a, 2)) / 5.0);
}
````

(b) Write a function that receives marks received by a student in 3 subjects and returns the average and percentage of these marks. Call this function from **main( )** and print the results in **main( )**.

````c
#include<stdio.h>
void marks(int, int, int, float *, float *);
int main(){
    int a, b, c;
    float avg, per;
    printf("Enter marks of 3 subjects: ");
    scanf("%d%d%d", &a, &b, &c);
    marks(a, b, c, &avg, &per);
    printf("Average = %f\nPercentage = %.2f %%", avg, per);
    return 0;
}
void marks(int i, int j, int k, float *av, float *pr){
    *av = (i + j + k) / 3.0;
    *pr = ((i + j + k) / 300.0) * 100.0;
}
````

(c) Write a C function to evaluate the series

<img src="https://render.githubusercontent.com/render/math?math=sin(x)=x-(x^3/3!)%2B(x^5/5!)-(x^7/7!)%2B...">

up to 10 terms.

````c
#include<stdio.h>
#include<math.h>

double sinx(float *);
double fact(int);

int main(){
    float x;
    double sum;
    printf("Enter 'x' in radians: ");
    scanf("%f", &x);
    printf("Sum of series...\n");
    sum= sinx(&x);
    printf("\n= %.6lf\n", sum);
    return 0;
}

double sinx(float *r){
    int i, j=2;
    double s = *r;
    printf("x");
    for(i = 3; i < 20; i = i + 2){
        if(j % 2 != 0){
            s = s + pow(*r, i) / fact(i);
            printf("+(x^%d/%d!)", i, i);
        }
        else{
            s = s - pow(*r, i) / fact(i);
            printf("-(x^%d/%d!)", i, i);
        }
        j++;
    }
    return s;
}

double fact(int a){
    int k;
    double f = 1;
    for(k = a; k > 0; k--){
        f = f * k;
    }
    return f;
}
````

(d) Given three variables **x**, **y**, **z** write a function to circularly shift their values to right. In other words if x = 5, y = 8, z = 10, after circular shift y = 5, z = 8, x =10. Call the function with variables **a**, **b**, **c** to circularly shift values.

````c
#include<stdio.h>
void circular_shift(int *, int *, int *);
int main(){
    int x, y, z;
    printf("Enter values of x, y and z: ");
    scanf("%d%d%d", &x, &y, &z);
    circular_shift(&x, &y, &z);
    printf("x=%d\ty=%d\tz=%d\n",x, y, z);
    return 0;
}
void circular_shift(int *a, int *b, int *c){
    int t;
    t = *c;
    *c = *b;
    *b = *a;
    *a = t;
}
````

(e) If the lengths of the sides of a triangle are denoted by a, b, and c, then area of triangle is given by

<img src="https://render.githubusercontent.com/render/math?math=area = \sqrt{S(S-a)(S-b)(S-c)}">

where, S = ( a + b + c ) / 2. Write a function to calculate the area of the triangle.

````c
#include<stdio.h>
#include<math.h>
float area_triangle(int *,int *,int *);
int main(){
    int a, b, c;
    float area;
    printf("Enter 3 sides of triangle: ");
    scanf("%d%d%d", &a, &b, &c);
    area = area_triangle(&a, &b, &c);
    printf("Area of triangle = %f square units.", area);
    return 0;
}
float area_triangle(int *x, int *y, int *z){
    float s, ar;
    s = (*x + *y + *z) / 2.0;
    ar = sqrt(s*(s-*x)*(s-*y)*(s-*z));
    return ar;
}
````

(f) Write a function to compute the distance between two points and use it to develop another function that will compute the area of the triangle whose vertices are **A(x1, y1)**, **B(x2, y2)**, and **C(x3, y3)**. Use these functions to develop a function which returns a value 1 if the point **(x, y)** lines inside the triangle ABC, otherwise returns a value 0.

````c
#include<stdio.h>
#include<math.h>

float distance(int *, int *, int *, int*);
float tri_area(float *, float *, float *);

int main(){
    int x, y, x1, y1, x2, y2, x3, y3;
    float dist12, dist23, dist13, dist01, dist02, dist03;
    float area, area1, area2, area3, total_area;

    printf("Enter point 1: ");
    scanf("%d%d", &x1, &y1);
    printf("Enter point 2: ");
    scanf("%d%d", &x2, &y2);
    dist12 = distance(&x1, &y1, &x2, &y2);
    printf("\nDistance between (%d, %d) and (%d, %d) = %.2f units\n", x1, y1, x2, y2, dist12);

    printf("Enter point 3: ");
    scanf("%d%d", &x3, &y3);

    dist13 = distance(&x1, &y1, &x3, &y3);
    dist23 = distance(&x2, &y2, &x3, &y3);

    area = tri_area(&dist12,&dist23,&dist13);
    printf("\nArea of triangle A(%d, %d), B(%d, %d) and C(%d, %d)= %.2f sq units\n",x1,y1,x2,y2,x3,y3,area);

    printf("\nEnter new point: ");
    scanf("%d%d", &x, &y);

    dist01 = distance(&x, &y, &x1, &y1);
    dist02 = distance(&x, &y, &x2, &y2);
    dist03 = distance(&x, &y, &x3, &y3);

    area1 = tri_area(&dist02, &dist03, &dist23);
    area2 = tri_area(&dist01, &dist03, &dist13);
    area3 = tri_area(&dist01, &dist02, &dist12);

    total_area = area1 + area2 + area3;

    if(total_area == area){
        printf("\n1 --> Point (%d, %d) lies inside triangle.\n", x, y);
    }
    else{
        printf("\n0 --> Point (%d, %d) does not lie inside triangle.\n", x, y);
    }
    return 0;
}

float distance(int *p1, int *q1, int *p2, int *q2){
    float d;
    d = sqrt(pow(*p2-*p1,2) + pow(*q2-*q1,2));
    return d;
}

float tri_area(float *d1, float *d2, float *d3){
    float s, a;
    s = (*d1 + *d2 + *d3)/2.0;
    a = sqrt(s*(s-*d1)*(s-*d2)*(s-*d3));

    //for comparing float upto 2 decimal places
    a = (int)(a * 100 + 0.5);
    a = (float)a / 100;

    return a;
}
````

(g) Write a function to compute the greatest common divisor given by Euclid’s algorithm, exemplified for J = 1980, K = 1617 as follows:

1980 / 1617 = 1 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1980 – 1 * 1617 = 363

1617 / 363 = 4 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1617 – 4 * 363 = 165

363 / 165 = 2 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 363 – 2 * 165 = 33

5 / 33 = 5 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 165 – 5 * 33 = 0

Thus, the greatest common divisor is 33.

````c
#include<stdio.h>
int euclid(int *, int *);
int main(){
    int j, k, f;
    printf("Enter values of J and K: ");
    scanf("%d%d", &j, &k);
    f = euclid(&j, &k);
    printf("GCD = %d\n", f);
    return 0;
}
int euclid(int *a, int *b){
    int c,t;
    do{
        c = *a/ *b;
        t = *a - (c * *b);
        *a = *b;
        *b = t;
    }while(t > 0);
    return *a;
}
````

