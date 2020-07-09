# [D] Answer the following:

(a) Write a function to calculate the factorial value of any integer entered through the keyboard.

````c
#include<stdio.h>
int factorial(int);
int main(){
    int n, f;
    printf("Enter a number: ");
    scanf("%d", &n);
    f = factorial(n);
    printf("Factorial of %d is %d\n", n, f);
    return 0;
}
int factorial(int x){
    int fact = 1, i;
    for(i = x; i > 0; i--){
        fact = fact * i;
    }
    return fact;
}
````



(b) Write a function **power ( a, b )**, to calculate the value of **a** raised to **b**.

````c
#include<stdio.h>
double power(int, int);
int main(){
    int a, b;
    double raise;
    printf("Enter a and b such that a^b: ");
    scanf("%d%d", &a, &b);
    raise = power(a, b);
    printf("%d ^ %d = %lf", a, b, raise);
    return 0;
}
double power(int x, int y){
    int i;
    double mul = 1;
    for(i = 0; i < y; i++){
        mul = mul * x;
    }
    return mul;
}
````



(c) Write a general-purpose function to convert any given year into its Roman equivalent. Use these Roman equivalents for decimal numbers:

````
1 – I, 5 – V, 10 – X, 50 – L, 100 – C, 500 – D, 1000 – M.
````

Example:

Roman equivalent of 1988 is mdcccclxxxviii. 

Roman equivalent of 1525 is mdxxv.

````c
#include<stdio.h>
void roman(int);
void rom(int, char);
int main(){
    int year;
    printf("Enter a year: ");
    scanf("%d", &year);
    printf("Roman equivalent of %d is ", year);
    roman(year);
    printf("\n");
    return 0;
}
void roman(int year){
    int m = year / 1000;
    year = year % 1000;
    rom(m, 'm');
    int d = year / 500;
    year = year % 500;
    rom(d, 'd');
    int c = year / 100;
    year = year % 100;
    rom(c, 'c');
    int l = year / 50;
    year = year % 50;
    rom(l, 'l');
    int x = year / 10;
    year = year % 10;
    rom(x, 'x');
    int v = year / 5;
    year  = year % 5;
    rom(v, 'v');
    int i = year;
    rom(i, 'i');
}
void rom(int r, char s){
    int i;
    for(i = 0; i < r; i++){
        printf("%c", s);
    }
}
````



(d) Any year is entered through the keyboard. Write a function to determine whether the year is a leap year or not.

````c
#include<stdio.h>
void leap(int);
int main(){
    int year;
    printf("Enter a year: ");
    scanf("%d", &year);
    leap(year);
    return 0;
}
void leap(int year){
    if( year % 4 == 0 && year % 100 != 0 || year % 400 == 0 )
        printf("Leap Year");
    else
        printf("Not a Leap Year");
}
````



(e) A positive integer is entered through the keyboard. Write a function to obtain the prime factors of this number.

For example, prime factors of 24 are 2, 2, 2 and 3, whereas prime factors of 35 are 5 and 7.

````c
#include<stdio.h>
int primefactor(int);
int main(){
    int n, x;
    printf("Enter a positive number: ");
    scanf("%d", &n);
    printf("Prime Factors of %d are: ", n);
    do{
        x = primefactor(n);
        printf("%d  ", x);
        n = n / x;
    }while(n > 1);
}
int primefactor(int n){
    int i;
    for(i = 2; i < n; i++){
        if(n % i == 0)
            return i;
    }
}
````
