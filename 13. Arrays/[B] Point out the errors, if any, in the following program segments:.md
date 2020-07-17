# [B] Point out the errors, if any, in the following program segments:

(a)

````c
/* mixed has some char and some int values */
# include <stdio.h>
int char mixed[ 100 ] ;
int main( )
{
    int a[ 10 ], i ;
    for ( i = 1 ; i <= 10 ; i++ )
    {
    	scanf ( "%d", a[ i ] ) ;
	    printf ( "%d\n", a[ i ] ) ;
    }
    return 0 ;
}
````

The subscript of the array `a` should vary from `0 to 9` whereas in the `for` loop, it varies from `1 to 10`. Here, the element at `a[0]` will hold a `garbage` value.

(b)

````c
# include <stdio.h>
int main( )
{
    int size ;
    scanf ( "%d", &size ) ;
    int arr[ size ] ;
    for ( i = 1 ; i <= size ; i++ )
    {
    	scanf ( "%d", &arr[ i ] ) ;
	    printf ( "%d\n", arr[ i ] ) ;
    }
    return 0 ;
}
````

The subscript of the array `arr` should begin from `0` and end at `size - 1` in the `for` loop. Here, the element at `arr[0]` will hold a `garbage` value.

(c)

````c
# include <stdio.h>
int main( )
{
    int i, a = 2, b = 3 ;
    int arr[ 2 + 3 ] ;
    for ( i = 0 ; i < a+b ; i++ )
    {
	    scanf ( "%d", &arr[ i ] ) ;
    	printf ( "%d\n", arr[ i ] ) ;
    }
    return 0 ;
}
````

**No error**.

