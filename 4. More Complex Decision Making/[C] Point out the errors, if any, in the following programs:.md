# [C] Point out the errors, if any, in the following programs:

(a)

````c
#include <stdio.h>
int main( )
{
    int code, flag ;
    if ( code == 1 & flag == 0 )
    	printf ( "The eagle has landed\n" ) ;
    return 0 ;
}
````

Use **Logical Operator** `&&` instead of  `&` in the `if` statement.

(b)

````c
#include <stdio.h>
int main( )
{
    char spy = 'a', password = 'z' ;
    if ( spy == 'a' or password == 'z' )
    	printf ( "All the birds are safe in the nest\n" ) ;
    return 0 ;
}
````

There is no `or` keyword in C. Instead use `||`.

(c)

````c
#include <stdio.h>
int main( )
{
    int i = 10, j = 20 ;
    if ( i = 5 ) && if ( j = 10 )
    	printf ( "Have a nice day\n" ) ;
    return 0 ;
}
````

Two `if` statements cannot be logically operated. Use  **Relational Operator** `==` instead of **Assignment Operator** `=` in the `if` statement.

Correct statement would be `if ( i == 5  &&  j == 10 )`.

(d)

````c
#include <stdio.h>
int main( )
{
    int x = 10, y = 20 ;
    if ( x >= 2 and y <= 50 )
    	printf ( "%d\n", x ) ;
    return 0 ;
}
````

There is no `and` keyword in C. Instead use `&&`.

(e)

````c
#include <stdio.h>
int main( )
{
    int x = 2 ;
    if ( x == 2 && x != 0 ) ;
    	printf ( "Hello\n" ) ;
    else
    	printf ( "Bye\n" ) ;
    return 0 ;
}
````

The `if` statement must not be terminated with a semicolon `;`.

(f)

````c
#include <stdio.h>
int main( )
{
    int i = 10, j = 10 ;
    if ( i && j == 10 )
    	printf ( "Have a nice day\n" ) ;
    return 0 ;
}
````

**No error**

(g)

````c
#include <stdio.h>
int main( )
{
    int j = 65 ;
    printf ( "j >= 65 ? %d : %c\n", j ) ;
    return 0 ;
}
````

**No error**

NOTE : Two arguments are required in the `printf` statement since it suggests `%d` as well as `%c`.

(h)

````c
#include <stdio.h>
int main( )
{
    int i = 10, j ;
    i >= 5 ? j = 10 : j = 15 ;
    printf ( "%d %d\n", i, j ) ;
    return 0 ;
}
````

**Lvalue required** error. Use parentheses in the **Conditional Operator**.

`i >= 5 ? ( j = 10 ) : ( j = 15 ) ;`

(i)

````c
#include <stdio.h>
int main( )
{
    int a = 5, b = 6 ;
    ( a == b ? printf ( "%d\n", a ) ) ;
    return 0 ;
}
````

There must be a `:` operator along with the `?` operator.

(j)

````c
#include <stdio.h>
int main( )
{
    int n = 9 ;
    ( n == 9 ? printf ( "Correct\n" ) ; : printf ( "Wrong\n" ) ; ) ;
    return 0 ;
}
````

The `printf` statement must not end with a semicolon `;` in the **Conditional Operator**.

