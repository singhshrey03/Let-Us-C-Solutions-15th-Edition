# [B] Attempt the following:

(a) Write a program to calculate overtime pay of 10 employees. Overtime is paid at the rate of Rs. 12.00 per hour for every hour worked above 40 hours. Assume that employees do not work for fractional part of an hour.

````c
#include<stdio.h>
int main(){
    int n,i,p;
    i=0;
    while(i++ < 10){
        printf("Enter work hours : ");
        scanf("%d", &n);
        if(n > 40){
           n = n - 40;
           p = n * 12;
           printf("Overtime pay is Rs. %d\n", p);
        }
        else{
            printf("NO Overtime Pay\n");
        }
    }
    return 0;
}
````

(b) Write a program to find the factorial value of any number entered through the keyboard.

````c
#include<stdio.h>
int main(){
    int n,num,fact;
    fact = 1;
    printf("Enter no. : ");
    scanf("%d", &n);
    num = n;
    while(n > 0){
        fact = fact * n;
        n--;
    }
    printf("Factorial of %d is %d", num, fact);
    return 0;
}
````

(c) Two numbers are entered through the keyboard. Write a program to find the value of one number raised to the power of another.

````c
#include<stdio.h>
int main(){
    int n1, n2, pow;
    printf("Enter 2 numbers : ");
    scanf("%d%d", &n1, &n2);
    pow = n1;
    if(n2 == 0){
        printf("1");
    }
    else{
        while(n2 > 1){
            pow = pow*n1;
            n2--;
        }
        printf("%d", pow);
    }
    return 0;
}
````

(d) Write a program to print all the ASCII values and their equivalent characters using a while loop. The ASCII values vary from 0 to 255.

````c
#include<stdio.h>
int main(){
    int n;
    n = 0;
    while(n < 256){
        printf("%d --> %c\n", n, n);
        n++;
    }
    return 0;
}
````

(e) Write a program to print out all Armstrong numbers between 1 and 500. If sum of cubes of each digit of the number is equal to the number itself, then the number is called an Armstrong number. For example, 153 = ( 1 * 1 * 1 ) + ( 5 * 5 * 5 ) + ( 3 * 3 * 3 ).

````c
#include<stdio.h>
#include<math.h>
int main(){
    int n, t, s, arm;
    n = 1;
    while(n <= 500){
        t = n;
        arm = 0;
        while(t != 0){
            s = t % 10;
            t = t / 10;
            arm = arm + pow(s, 3);
        }
        if(arm == n){
            printf("%d\n", n);
        }
        n++;
    }
    return 0;
}
````

(f) Write a program for a matchstick game being played between the computer and a user. Your program should ensure that the computer always wins. Rules for the game are as follows:

<ul>
    <li>There are 21 matchsticks.</li>
    <li>The computer asks the player to pick 1, 2, 3, or 4 matchsticks.</li>
    <li>After the person picks, the computer does its picking.</li>
    <li>Whoever is forced to pick up the last matchstick loses the game.</li>
</ul>

````c
//Idea is to think for 20 matchsticks as the user who would pick the last one will lose the game.
//Divide 20 into four parts that is, each part is of size 5.
//So if the computer picks x matchsticks then the user should pick (5 - x) matchsticks and should proceed in the same way.
//In this way, 20 matchsticks will be used and the last matchstick would be picked by the computer.

#include<stdio.h>
int main(){
    int user,n;
    n = 21;
    while(n > 1){
        printf("Enter no. of matchsticks from 1-4 : ");
        scanf("%d", &user);
        n = n - user;
        printf("Matchsticks left : %d\n", n);
        printf("Computer Entered : %d\n", 5-user);
        n = n - (5 - user);
        printf("Matchsticks left : %d\n", n);
    }
    printf("**********COMPUTER WINS !!!**********");
    return 0;
}
````

(g) Write a program to enter numbers till the user wants. At the end it should display the count of positive, negative and zeros entered.

````c
#include<stdio.h>
int main(){
    int n,cn,cz,cp,choice;
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

(h) Write a program to receive an integer and find its octal equivalent.

(Hint: To obtain octal equivalent of an integer, divide it continuously by 8 till dividend doesn’t become zero, then write the remainders obtained in reverse direction.)

````c
#include<stdio.h>
int main(){
    int dec,oct,rev;
    oct = 0;
    rev = 0;
    printf("Enter an integer : ");
    scanf("%d", dec);
    while(dec != 0){
        oct = oct * 10 + dec % 8;
        dec = dec / 8;
    }
    while(oct != 0){
        rev = rev * 10 + oct % 10;
        oct = oct / 10;
    }
    printf("%d",rev);
    return 0;
}
````

(i) Write a program to find the range of a set of numbers entered through the keyboard. Range is the difference between the smallest and biggest number in the list.

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

