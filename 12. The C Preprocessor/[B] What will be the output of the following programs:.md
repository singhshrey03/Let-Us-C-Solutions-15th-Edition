# [B] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int i = 2 ;
    # ifdef DEF
    	i *= i ;
    # else
    	printf ( "%d\n", i ) ;
    # endif
    return 0 ;
}
````

````
2

````

(b)

````c
# include <stdio.h>
# define PRODUCT(x) ( x * x )
int main( )
{
    int i = 3, j, k, l ;
    j = PRODUCT( i + 1 ) ;
    k = PRODUCT( i++ ) ;
    l = PRODUCT ( ++i ) ;
    printf ( "%d %d %d %d\n", i, j, k, l ) ;
    return 0 ;
}
````

````
7 7 12 49

````

(c)

````c
# include <stdio.h>
# define PI 3.14
# define AREA( x, y, z ) ( PI * x * x + y * z ) ;
int main( )
{
    float a = AREA ( 1, 5, 8 ) ;
    float b = AREA ( AREA ( 1, 5, 8 ), 4, 5 ) ;
    printf ( " a = %f\n", a ) ;
    printf ( " b = %f\n", b ) ;
    return 0 ;
}
````

````
a = 43.139999
b = 5863.727051

````

