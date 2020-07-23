# [H] State True or False:

(a) Address of a floating-point variable is always a whole number.

````
True
````

(b) Which of the following is the correct way of declaring a float pointer:

1. float ptr ;
2. float *ptr ;
3. *float ptr ;
4. None of the above

````
2. float *ptr ;
````

(c) Add the missing statement for the following program to print 35:

````c
#include <stdio.h>
int main( )
{
    int j, *ptr ;
    *ptr = 35 ;
    printf ( "%d\n", j ) ;
    return 0 ;
}
````

````c
#include <stdio.h>
int main( )
{
    int j, *ptr ;
    ptr = &j ;
    *ptr = 35 ;
    printf ( "%d\n", j ) ;
    return 0 ;
}
````



(d) if **int s[ 5 ]** is a one-dimensional array of integers, which of the following refers to the third element in the array?

1. *( s + 2 )
2. *( s + 3 )
3. s + 3
4. s + 2

````
1. *( s + 2 )
````

