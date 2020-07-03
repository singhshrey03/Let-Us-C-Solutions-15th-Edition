# [B] Point out the errors, if any, in the following programs:

(a) 

````c
#include <stdio.h>
int main( )
{
    float a = 12.25, b = 12.52 ;
    if ( a = b )
    	printf ( "a and b are equal\n" ) ;
    return 0 ;
}
````

**No error.**


(b)

````c
#include <stdio.h>
int main( )
{
    int j = 10, k = 12 ;
    if ( k >= j )
    {
    	{
            k = j ;
            j = k ;
        }
    }
    return 0 ;
}
````

**No error.**

(c)

````c
#include <stdio.h>
int main( )
{
    if ( 'X' < 'x' )
        printf ( "ascii value of X is smaller than that of x\n" ) ;
}
````

**No error.**

(d)

````c
#include <stdio.h>
int main( )
{
    int x = 10 ;
    if ( x >= 2 ) then
    	printf ( "%d\n", x ) ;
    return 0 ;
}
````

There is no keyword `then` in C.

(e)

````c
#include <stdio.h>
int main( )
{
    int x = 10, y = 15 ;
    if ( x % 2 = y % 3 )
        printf ( "Carpathians\n" ) ;
}
````

Use `==` instead of `=` in the `if` statement. 

(f)

````c
#include <stdio.h>
int main( )
{
    int x = 30, y = 40 ;
    if ( x == y )
    	printf ( "x is equal to y\n" ) ;
    elseif ( x > y )
    	printf ( "x is greater than y\n" ) ;
    elseif ( x < y )
      	printf ( "x is less than y\n" ) ;
    return 0 ;
}
````

There must be a space between `else` and `if` in the `elseif`.

(g)

````c
#include <stdio.h>
int main( )
{
    int a, b ;
    scanf ( "%d %d", a, b ) ;
    if ( a > b ) ;
    	printf ( "This is a game\n" ) ;
    else
      	printf ( "You have to play it\n" ) ;
    return 0 ;
}
````

Use of **Address of  (&)** operator is must before variables in `scanf()`.

