# [D] Attempt the following:

(1) Define a function that receives 4 integers and returns sum, product and average of these integers.

````c
#include<stdio.h>
void calc(int ,int, int, int , float *, float *, float *);
int main(){
    int a,b,c,d;
    float sum, prod, avg;

    printf("Enter 4 integers: ");
    scanf("%d%d%d%d",&a,&b,&c,&d);

    calc(a,b,c,d,&sum,&prod,&avg);

    printf("Sum = %f\n", sum);
    printf("Product = %f\n", prod);
    printf("Average = %f\n", avg);

    return 0;
}
void calc(int a, int b, int c, int d, float *sum, float *prod, float *avg){
    *sum = a+b+c+d;
    *prod = a*b*c*d;
    *avg = *sum/4.0;
}
````



(2) Write a recursive function which prints the prime factors of the number that it receives when called from main( ).

````c
#include<stdio.h>
int prime_factors(int);
int main(){
    int n;
    printf("Enter a number: ");
    scanf("%d",&n);
    printf("Prime factors of %d are... ",n);
    prime_factors(n);
    return 0;
}
int prime_factors(int x){
    int i;
    for(i=2;i<=x;i++){
        if(x%i==0){
            printf("%d  ",i);
            prime_factors(x/i);
            break;
        }
    }
    return 0;
}
````



(3) Write macros for calculating area of circle, circumference of circle, volume of a cone and volume of sphere.

````c
#define PI 3.141592
#define AREACIRCLE(r) (PI*r*r)
#define CIRCUMCIRCLE(r) (2*PI*r)
#define VOLCONE(r,h) (PI*r*r*h/3)
#define VOLSPHERE(r) (4*PI*r*r*r/3)

#include<stdio.h>
int main(){
    int r,h;
    float areac, circ, volc, vols;
    printf("Enter radius and height: ");
    scanf("%d%d", &r, &h);

    areac = AREACIRCLE(r);
    circ = CIRCUMCIRCLE(r);
    volc = VOLCONE(r,h);
    vols = VOLSPHERE(r);

    printf("Area of Circle = %f\n",areac);
    printf("Circumference of Circle = %f\n",circ);
    printf("Volume of Cone = %f\n",volc);
    printf("Volume of Sphere = %f\n",vols);

    return 0;
}
````



(4) Write a program that prints sizes of all types of chars, ints and reals.

````c
#include<stdio.h>
int main(){
    char c;
    unsigned char d;
    int i;
    unsigned int j;
    short int k;
    unsigned short int l;
    long int m;
    unsigned long int n;
    float x;
    double y;
    long double z;

    printf("char = %d byte(s)\n",sizeof(c));
    printf("unsigned char = %d byte(s)\n",sizeof(d));
    printf("int = %d byte(s)\n",sizeof(i));
    printf("unsigned int = %d byte(s)\n",sizeof(j));
    printf("short int = %d byte(s)\n",sizeof(k));
    printf("unsigned short int = %d byte(s)\n",sizeof(l));
    printf("long int = %d byte(s)\n",sizeof(m));
    printf("unsigned long int = %d byte(s)\n",sizeof(n));
    printf("float = %d byte(s)\n",sizeof(x));
    printf("double = %d byte(s)\n",sizeof(y));
    printf("long double = %d byte(s)\n",sizeof(z));

    return 0;
}
````

