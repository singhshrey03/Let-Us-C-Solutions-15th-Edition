# [E] Attempt the following:

(1) Write a program to calculate the sum of the following series:

````
1! 2! + 2! 3! + 3! 4! + 4! 5! + …… + 9! 10!
````

````c
#include<stdio.h>
int main(){
    int i, j;
    double sum = 0;
    printf("Sum of the series...\n");
    for(i = 1; i <= 9; i++){
        double f1 = 1,f2 = i + 1;
        for(j = i; j > 0; j--){
            f1 = f1 * j;
        }
        f2 = f2 * f1;
        sum = sum + f1 * f2;
        if(i<9)
            printf("%d!*%d! + ", i, i+1);
    }
    printf("9!*10!\n= %.0lf\n", sum);
}
````

(2) Write a program to enter the numbers till the user wants and at the end it should display the count of positive, negative and zeros entered.

````c
#include<stdio.h>
int main(){
    int n, cn, cz, cp, choice;
    cn = 0;
    cz = 0;
    cp = 0;
    choice = 1;
    while(choice == 1){
        printf("Enter a number : ");
        scanf("%d",&n);
        if(n > 0){
            cp++;
        }
        if(n == 0){
            cz++;
        }
        if(n < 0){
            cn++;
        }
        printf("Do you wish to continue?\t1 --> YES\t0 --> NO\n");
        scanf("%d", &choice);
    }
    printf("Negatives : %d\nZeros : %d\nPositives : %d", cn, cz, cp);
    return 0;
}
````

(3) Write a program to find the range of a set of numbers that are input through the keyboard. Range is the difference between the smallest and biggest number in the list.

````c
#include<stdio.h>
int main(){
    int min, max, n, choice;
    printf("Enter a no. : ");
    scanf("%d", &n);
    printf("Do you wish to continue?\t1 --> Yes\t0 --> No\n");
    scanf("%d", &choice);
    min = n;
    max = n;
    while(choice == 1){
        printf("Enter a no. : ");
        scanf("%d", &n);
        if(n < min){
            min = n;
        }
        if(n > max){
            max = n;
        }
        printf("Do you wish to continue?\t1 --> Yes\t0 --> No\n");
        scanf("%d", &choice);
    }
    printf("Range is (%d, %d)", min, max);
    return 0;
}
````

(4) If three integers are entered through the keyboard, write a program to determine whether they form a Pythogorean triplet or not.

````c
#include<stdio.h>
int main(){
    int i, j, k;
    printf("Enter 3 integers: ");
    scanf("%d%d%d", &i, &j, &k);
    if((i*i) + (j*j) == (k*k) || (i*i) + (k*k) == (j*j) || (k*k) + (j*j) == (i*i))
        printf("Yes! These 3 integers form a Pythogorean Triplet.\n");
    else
        printf("No! These 3 integers do not form a Pythogorean Triplet.\n");
    return 0;
}
````

