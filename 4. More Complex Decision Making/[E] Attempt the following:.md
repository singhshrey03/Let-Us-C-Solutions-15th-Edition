# [E] Attempt the following:

(a) Using conditional operators determine:

<ol>
<li>Whether the character entered through the keyboard is a lower case alphabet or not. </li>
<li>Whether a character entered through the keyboard is a special symbol or not.</li></ol>

````c
// Whether the character entered through the keyboard is a lower case alphabet or not.

#include<stdio.h>
int main(){
    char c;
    int n;
    printf("Enter a character : ");
    scanf("%c",&c);
    n = c;
    (n>=97 && n<=122)?(printf("Lowercase Alphabet")):(printf("Not Lowercase Alphabet"));
    return 0;
}
````

````c
// Whether the character entered through the keyboard is a lower case alphabet or not.

#include<stdio.h>
int main(){
    char c;
    int n;
    printf("Enter a character : ");
    scanf("%c",&c);
    n = c;
    n>=0 && n<=47 ? printf("Yes") : (n>=58 && n<=64 ? printf("Yes") : (n>=91 && n<=96 ? printf("Yes") : (n>=123 && n<=127 ? printf("Yes") : printf("No"))));
    return 0;
}
````

(b) Write a program using conditional operators to determine whether a year entered through the keyboard is a leap year or not.

````c
#include<stdio.h>
int main(){
    int n;
    printf("Enter year : ");
    scanf("%d",&n);
    n % 4 == 0 ? (n % 100 == 0 ? (n % 400 == 0 ? printf("Leap year") : printf("Not a leap year")) : printf("Not a leap year")) : printf("Not a leap year");
    return 0;
}
````

(c) Write a program to find the greatest of the three numbers entered through the keyboard. Use conditional operators.

````c
#include<stdio.h>
int main(){
    int a, b, c, mx;
    printf("Enter 3 digits : ");
    scanf("%d%d%d", &a, &b, &c);
    mx = (a > b ? (a > c ? a : c) : (b > c ? b : c));
    printf("Greatest of above is %d", mx);
    return 0;
}
````

(d) Write a program to receive value of an angle in degrees and check whether sum of squares of sine and cosine of this angle is equal to 1.

````c
#include<stdio.h>
#include<math.h>
int main(){
    float deg, sum;
    printf("Enter angle in  degrees : ");
    scanf("%f", &deg);
    deg = deg * 3.1415926535 / 180.0;
    sin(deg)*sin(deg) + cos(deg)*cos(deg) == 1 ? printf("Yes") : printf("No");
    return 0;
}
````

(e) Rewrite the following program using conditional operators.

````
#include <stdio.h>
int main( )
{
    float sal ;
    printf ( "Enter the salary" ) ;
    scanf ( "%f", &sal ) ;
    if ( sal >= 25000 && sal <= 40000 )
    	printf ( "Manager\n" ) ;
    else
    	if ( sal >= 15000 && sal < 25000 )
    		printf ( "Accountant\n" ) ;
    	else
    		printf ( "Clerk\n" ) ;
    return 0 ;
}
````

````c
#include<stdio.h>
int main(){
    float sal;
    printf("Enter the salary : ");
    scanf("%f", &sal);
    sal >= 25000 && sal <= 40000 ? printf("Manager"): sal>=15000 && sal<25000 ? printf("Accountant") : printf("Clerk");
    return 0;
}
````

