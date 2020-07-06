# [C] Attempt the following:

(a) Write a program to print all prime numbers from 1 to 300. (Hint: Use nested loops, **break** and **continue**)

````c
#include<stdio.h>
int main(){
    int i, j;
    for(i = 1; i <= 300; i++){
        for(j = 2; j < i; j++){
            if(i % j == 0){
                break;
            }
        }
        if(i == j){
            printf("%d\n", i);
        }
    }
    return 0;
}
````

(b) Write a program to fill the entire screen with a smiling face. The smiling face has an ASCII value 1.

````c
#include<stdio.h>
int main(){
    for(; ;){
        printf("%c", 1);
    }
    return 0;
}
````

(c) Write a program to add first seven terms of the following series using a **for** loop:

<img src="https://render.githubusercontent.com/render/math?math=\frac{1}{1!}%2B\frac{2}{2!}%2B\frac{3}{3!}%2B.....">

````c
#include<stdio.h>
int main(){
    float sum = 0;
    for(int i = 1; i <= 7; i++){
        float fact = 1;
        for(int j = i; j > 0; j--){
            fact = fact * j;
        }
        sum = sum + i / fact;
    }
    printf("%f", sum);
    return 0;
}
````

(d) Write a program to generate all combinations of 1, 2 and 3 using **for** loop.

````c
#include<stdio.h>
int main(){
    int i, j, k;
    for(i=1; i<4; i++){
        for(j=1; j<4; j++){
            for(k=1; k<4; k++){
                if(i==j || i==k || j==k){
                    continue;
                }
                else{
                    printf("%d\n",i*100 + j*10 + k);
                }
            }
        }
    }
    return 0;
}
````

(e) A machine is purchased which will produce earning of Rs. 1000 per year while it lasts. The machine costs Rs. 6000 and will have a salvage value of Rs. 2000 when it is condemned. If 9 percent per annum can be earned on alternate investments, write a program to determine what will be the minimum life of the machine to make it a more attractive investment compared to alternative investment?

````c
#include<stdio.h>
int main()
{
    int year=1, invest, alternate, net_invest;
    do
    {
        alternate = 90 * year;
        invest = 1000 * year;
        net_invest = invest - 6000 + 2000;
        year++;
    }while(alternate>net_invest);
    
    printf("Minimum life of machine: %d years", year);
}
````

(f) Write a program to print the multiplication table of the number entered by the user. The table should get displayed in the following form:

29 * 1 = 29

29 * 2 = 58

…

````c
#include<stdio.h>
int main(){
    int i, n;
    printf("Enter a number: ");
    scanf("%d", &n);
    for(i = 1; i <= 12; i++){
        printf("%d * %d = %d\n", n, i, n*i);
    }
    return 0;
}
````

(g) According to a study, the approximate level of intelligence of a person can be calculated using the formula: 

i = 2 + ( y + 0.5 x ) 

Write a program which will produce a table of values of **i**, **y** and **x**, where **y** varies from 1 to 6, and, for each value of **y**, **x** varies from 5.5 to 12.5 in steps of 0.5 .

````c
#include<stdio.h>
int main(){
    int y;
    float i, x;
    printf("i\t\ty\tx\n");
    for(y = 1; y <= 6; y++){
        for(x = 5.5; x < 12.6; ){
            printf("%f\t%d\t%f\n", 2+(y + 0.5*x), y, x);
            x = x + 0.5;
        }
    }
    return 0;
}
````



(h) When interest compounds q times per year at an annual rate of r % for n years, the principal p compounds to an amount a as per the following formula

a = p ( 1 + r / n ) <sup>nq</sup>

Write a program to read 10 sets of **p, r, n** & **q** and calculate the corresponding **a**.

````c
#include<stdio.h>
#include<math.h>
int main(){
    float a;
    int p,r,n,q;
    for(int i=1;i<=10;i++){
        printf("Enter values of p, r, n, q : ");
        scanf("%d%d%d%d", &p, &r, &n, &q);
        a = p* pow(1.0+ (r/100.0)/(n*(1.0)),n*q);
        printf("Interest is %f\n", a);
    }
    return 0;
}
````

(i) The natural logarithm can be approximated by the following series.

<img src="https://render.githubusercontent.com/render/math?math=\frac{x-1}{x}%2B\frac{1}{2}(\frac{x-1}{x})^2%2B\frac{1}{2}(\frac{x-1}{x})^3%2B\frac{1}{2}(\frac{x-1}{x})^4%2B....">

If **x** is input through the keyboard, write a program to calculate the sum of first seven terms of this series.

````c
#include<stdio.h>
#include<math.h>
int main(){
    int x;
    float y, sum, term;
    printf("Enter a number : ");
    scanf("%d", &x);
    sum = (x - 1) / (x * 1.0);
    term = sum;
    for(int i = 2; i <= 6; i++){
        sum = sum + 0.5 * pow(term, i);
    }
    printf("%f", sum);
    return 0;
}
````

(j) Write a program to generate all Pythogorean Triplets with side length less than or equal to 30.

````c
#include<stdio.h>
int main(){
    int i, j, k;
    for(i = 1; i <= 30; i++){
        for(j = i; j <= 30; j++){
            for(k = j; k <= 30; k++){
                if((i * i) + (j * j) == (k * k)){
                    printf("%d %d %d\n",i, j, k);
                }
            }
        }
    }
    return 0;
}
````

(k) Population of a town today is 100000. The population has increased steadily at the rate of 10 % per year for last 10 years. Write a program to determine the population at the end of each year in the last decade.

````c
#include<stdio.h>
int main(){
    int i, n = 100000;
    for(i = 10; i >= 1; i--){
        printf("Population in year %d is %d\n", i, n);
        n = 0.9 * n;
    }
    return 0;
}
````

(l) Ramanujan number is the smallest number that can be expressed as sum of two cubes in two different ways. Write a program to print all such numbers up to a reasonable limit.

````c
#include<stdio.h>
#include<math.h>
int main(){
    int i, j, k, n, count;
    printf("Enter a number : ");
    scanf("%d", &n);
    for(i = 1; i <= n; i++){
        count = 0;
        for(j = 1; j*j*j <= n; j++){
            for(k = j; j*j*j + k*k*k <= n; k++){
                if(j*j*j + k*k*k == i){
                    count++;
                    if(count > 1){
                        printf("%d\n", i);
                    }
                }
            }
        }
    }
    return 0;
}
````

(m) Write a program to print 24 hours of day with suitable suffixes like AM, PM, Noon and Midnight.

````c
#include<stdio.h>
int main(){
    int n;
    for(n = 0; n <= 24; n++){
        if(n > 0 && n < 12){
            printf("%d AM\n", n);
        }
        if(n > 12 && n < 24){
            printf("%d PM\n", n);
        }
        if(n == 12){
            printf("%d NOON\n", n);
        }
        if(n == 0){
            printf("%d MIDNIGHT\n", n);
        }
    }
    return 0;
}
````

(n) Write a program to produce the following output:

````
      1
    2   3
  4   5   6
7   8   9   10
````

````c
#include<stdio.h>
int main(){
    int i, j, k, n, num;
    num = 1;
    printf("Enter a number : ");
    scanf("%d", &n);
    for(i = 1; i <= n; i++){		

        for(j = n; j > i; j--){
            printf("\t");
        }

        for(k = 1; k <= i; k++){
            printf("%d\t\t", num++);	
        }
        printf("\n");
    }
    return 0;
}
````

(o) Write a program to produce the following output:

````
A B C D E F G F E D C B A
A B C D E F   F E D C B A
A B C D E       E D C B A
A B C D           D C B A
A B C               C B A
A B                   B A
A                       A
````

````c
#include<stdio.h>
int main(){
    int i, j, k, n, s;
    n = 7;
    for(i = 0; i < n; i++){

        for(j = 0;j < n-i; j++){
            printf("%c ", 65 + j);
        }

        for(s = 0;s < (i-1)*2+1; s++){
            printf("  ");
        }

        for(k = j-1; k >= 0; k--){
            if(k == n-1){
                continue;
            }
            printf("%c ", 65+k);
        }
        printf("\n");
    }
    return 0;
}
````

(p) Write a program to produce the following output:

````
        1
      1   1
    1   2   1
  1   3   3   1
1   4   6   4   1
````

````c
#include<stdio.h>
int main(){
    int i, j, k, n, no;
    no = 7;
    for(i = 0; i < no; i++){
        for(j = 0; j < no-i; j++){
            printf("  ");
        }
        n = 1;
        for(k = 0;k <= i; k++){
            printf("%d   ",n);
            n = n * (i - k) / (k + 1);
        }
        printf("\n");
    }
    return 0;
}
````

