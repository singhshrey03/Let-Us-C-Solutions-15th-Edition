# [B] Point out the errors, if any, in the following programs:

(a)

````c
# include <stdio.h>
int addmult ( int, int )
int main( )
{
    int i = 3, j = 4, k, l ;
    k = addmult ( i, j ) ;
    l = addmult ( i, j ) ;
    printf ( "%d %d\n", k, l ) ;
    return 0 ;
}
int addmult ( int ii, int jj )
{
    int kk, ll ;
    kk = ii + jj ;
    ll = ii * jj ;
    return ( kk, ll ) ;
}
````

1. Semicolon `;` missing in the function prototype declaration.

2. A function can return only one value at a time.

(b)

````c
# include <stdio.h>
void message( ) ;
int main( )
{
    int a ;
    a = message( ) ;
    return 0 ;
}
void message( )
{
    printf ( "Viruses are written in C\n" ) ;
    return ;
}
````

Return type of the function `message` is `void` but it is being collected in an `int` variable `a`.

(c)

````c
# include <stdio.h>
int main( )
{
    float a = 15.5 ;
    char ch = 'C' ;
    printit ( a, ch ) ;
    return 0 ;
}
printit ( a, ch )
{
    printf ( "%f %c\n", a, ch ) ;
}
````

1. Function prototype declaration missing.
2. No return type of the function `printit` is specified.

NOTE : Here the return type of function `printit`, data type of `a` and `ch` are defaulted to `int`.

(d)

````c
# include <stdio.h>
void message( ) ;
int main( )
{
    message( ) ;
    message( ) ;
    return 0 ;
}
void message( ) ;
{
    printf ( "Praise worthy and C worthy are synonyms\n" ) ;
}
````

Semicolon `;` must not be used in the function definition.

(e)

````c
# include <stdio.h>
int main( )
{
    let_us_c( )
    {
        printf ( "C is a Cimple minded language !\n" ) ;
        printf ( "Others are of course no match !\n" ) ;
    }
    return 0 ;
}
````

One function cannot be defined within another function.

(f)

````c
# include <stdio.h>
void message( ) ;
int main( )
{
    message ( message( ) ) ;
    return 0 ;
}
void message( )
{
    printf ( "It’s a small world after all…\n" ) ;
}
````

Function `message` with return type `void` and no `parameters` is passed within itself as a parameter.

