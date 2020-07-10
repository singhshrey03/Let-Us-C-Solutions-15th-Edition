# [B] Point out the errors, if any, in the following programs:

(a)

````c
# include <stdio.h>
void pass ( int, int ) ;
int main( )
{
    int i = 135, a = 135, k ;
    k = pass ( i, a ) ;
    printf ( "%d\n", k ) ;
    return 0 ;
}
void pass ( int j, int b )
int c ;
{
    c = j + b ;
    return ( c ) ;
}
````

1. `int c` must be declared within the function `pass`. 
2. Return type of the function `pass` is `void` but it is being collected in an `int` variable `k`.

(b)

````c
# include <stdio.h>
void jiaayjo ( int , int )
int main( )
{
    int p = 23, f = 24 ;
    jiaayjo ( &p, &f ) ;
    printf ( "%d %d\n", p, f ) ;
    return 0 ;
}
void jiaayjo ( int q, int g )
{
    q = q + q ;
    g = g + g ;
}
````

1. Semicolon `;` missing in the function prototype declaration.
2. `q` and `g` must be declared as integer pointer variables.

(c)

````c
# include <stdio.h>
void check ( int ) ;
int main( )
{
    int k = 35, z ;
    z = check ( k ) ;
    printf ( "%d\n", z ) ;
    return 0 ;
}
void check ( m )
{
    int m ;
    if ( m > 40 )
	    return ( 1 ) ;
    else
    	return ( 0 ) ;
}
````

The declaration of `m` in the function `check` will now hold a new garbage value.

(d)

````c
# include <stdio.h>
void function ( int * ) ;
int main( )
{
    int i = 35, *z ;
    z = function ( &i ) ;
    printf ( "%d\n", z ) ;
    return 0 ;
}
void function ( int *m )
{
    return ( *m + 2 ) ;
}
````

1. Return type of the function `function` is `void` but it is being collected in an `int` variable `z`.
2. `z` must not be declared as a pointer variable in the `main` funtion.

