# [B] Attempt the following:

(a) A 5-digit positive integer is entered through the keyboard, write a recursive and a non-recursive function to calculate sum of digits of the 5-digit number.

````c
#include<stdio.h>
int sums(int);
int main(){
    int n, sum;
    printf("Enter a 5 digit number: ");
    scanf("%d", &n);
    sum = sums(n);
    printf("Sum of digits = %d\n", sum);
    return 0;
}
int sums(int x){
    int s;
    if(x<=0){
        return 0;
    }
    else{
        s = (x % 10) + sums(x / 10);
    }
    return s;
}
````

(b) 

A positive integer is entered through the keyboard, write a program to obtain the prime factors of the number. Modify the function suitably to obtain the prime factors recursively.

````c
#include<stdio.h>
int prime_factors(int);
int main(){
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    printf("Prime factors of %d are... ", n);
    prime_factors(n);
    return 0;
}
int prime_factors(int x){
    int i;
    for(i = 2; i <= x; i++){
        if(x % i == 0){
            printf("%d  ", i);
            prime_factors(x / i);
            break;
        }
    }
    return 0;
}
````

(c) 

Write a recursive function to obtain the first 25 numbers of a Fibonacci sequence. In a Fibonacci sequence the sum of two successive terms gives the third term. Following are the first few terms of the Fibonacci sequence:
1 1 2 3 5 8 13 21 34 55 89...

````c
#include<stdio.h>
int fibo(int, int, int);
int main (){
    int a, b, n;
    a = 0, b = 1, n = 25;
    printf("%d\n%d\n", a, b);
    n = n - 2;
    fibo (a, b, n);
    return 0;
}
int fibo(int x, int y, int t){
    if(t == 0)
        return 0;
    printf ("%d\n", x + y);
    fibo(y, x+y, t-1);
}
````

OR

````c
#include<stdio.h>
int fibo(int);
int main(){
    int a, n;
    a = 0, n = 25;
    printf("First 25 terms of Fibonacci Series are...\n");
    for(a = 0; a < n; a++){
        printf("%d\n", fibo(a));
    }
}
int fibo(int x){
    if(x < 2)
        return x;
    else
        return(fibo(x-1) + fibo(x-2));
}
````

(d) A positive integer is entered through the keyboard, write a function to find the binary equivalent of this number :

1. Without using recursion
2. Using recursion 

````c
//1. Without using recursion

#include<stdio.h>
int binary_eq(int);
int main(){
    int n, b;
    printf("Enter a number: ");
    scanf("%d", &n);
    b = binary_eq(n);
    printf("Binary equivalent of %d is %d", n, b);
    return 0;
}
int binary_eq(int x){
    int b, i, t;
    b = 0, t = 1;
    while(x > 0){
        i = x % 2;
        x = x / 2;
        b = b + i*t;
        t = t * 10;
    }
    return b;
}
````

````c
//2. Using recursion

#include<stdio.h>
int binary_eq(int);
int main(){
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    printf("Binary equivalent of %d is ", n);
    binary_eq(n);
    return 0;
}
int binary_eq(int x){
    if(x <= 0)
        return 0;
    else{
        binary_eq(x / 2);
        printf("%d", x%2);
    }
}
````

(e) Write a recursive function to obtain the running sum of first 25 natural numbers.

````c
#include<stdio.h>
int sums(int);
int main(){
    int n, s;
    printf("Enter a number: ");
    scanf("%d", &n);
    s = sums(n);
    printf("Sum of first %d natural numbers is %d.\n", n, s);
    return 0;
}
int sums(int x){
    if(x == 0)
        return 0;
    else
        return(x + sums(x-1));
}
````

