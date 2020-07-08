# [D] Point out the error, if any, in the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int i = 10, j = 20 ;
    if ( i = 5) && if ( j = 10 )
    	printf ( "Have a nice day" ) ;
    return 0 ;
}
````

Two `if` statements cannot be logically operated. Use **Relational Operator** `==` instead of **Assignment Operator** `=` in the `if` statement.

Correct statement would be `if ( i == 5 && j == 10 )`.

(b)

````c
# include <stdio.h>
int main( )
{
    int x = 10 ;
    if ( x >= 2 ) then
    	printf ( "\n%d", x ) ;
    return 0 ;
}
````

There is no `then` keyword in C.

(c)

````c
# include <stdio.h>
int main( )
{
    int x = 0, y = 5, z = 10, a ;
    a = x > 1 ? y > 1 : z > 1 ? 100 : 200 : 300 ;
    printf ( "%d" , a ) ;
    return 0 ;
}
````

Incorrect use of **Conditional Operator**.

(d)

````c
# include <stdio.h>
int main( )
{
    int x = 0, y = 5, z ;
    float a = 1.5, b = 2.2, c ;
    z = x || b ;
    c = a && b ;
    printf ( "%d %f", z, c ) ;
    return 0 ;
}
````

**No error**

(e)

````c
# include <stdio.h>
int main( )
{
    int a = 10, b = 5, c ;
    c += a *= b ;
    printf ( "%d %d %d" , a, b, c ) ;
}
````

**No error**

