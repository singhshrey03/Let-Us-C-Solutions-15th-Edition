# [F] Point out the errors, if any, in the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int array[ 6 ] = { 1, 2, 3, 4, 5, 6 } ;
    int i ;
    for ( i = 0 ; i <= 25 ; i++ )
	    printf ( "%d\n", array[ i ] ) ;
    return 0 ;
}
````

The above `printf` statement will print `garbage` values after `6` elements in the `array`.

(b)

````c
# include <stdio.h>
int main( )
{
    int sub[ 50 ], i ;
    for ( i = 1 ; i <= 50 ; i++ )
    {
	    sub[ i ] = i ;
    	printf ( "%d\n" , sub[ i ] ) ;
    }
    return 0 ;
}
````

The subscript of the array `sub` should begin from `0` and end at `49` in the `for` loop. Here, the element at `sub[0]` will hold a `garbage` value.

(c)

````c
# include <stdio.h>
int main( )
{
    int a[ ] = { 10, 20, 30, 40, 50 } ;
    int j ;
    j = a ; /* store the address of zeroth element */
    j = j + 3 ;
    printf ( "%d\n" *j ) ;
    return 0 ;
}
````

Variable `j` must be `pointer` variable.

(d)

````c
# include <stdio.h>
int main( )
{
    float a[ ] = { 13.24, 1.5, 1.5, 5.4, 3.5 } ;
    float *j ;
    j = a ;
    j = j + 4 ;
    printf ( "%d %d %d\n", j, *j, a[ 4 ] ) ;
    return 0 ;
}
````

Incorrect use of `format specifiers` in the `printf` statement. It must be `%u %f %f`.

(e)

````c
# include <stdio.h>
int main( )
{
    int max = 5 ;
    float arr[ max ] ;
    for ( i = 0 ; i < max ; i++ )
	    scanf ( "%f", &arr[ i ] ) ;
    return 0 ;
}
````

**No Error**. Integer variable `i` needs to be declared.
