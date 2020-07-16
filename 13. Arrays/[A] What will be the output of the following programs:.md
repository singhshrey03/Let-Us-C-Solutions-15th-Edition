# [A] What will be the output of the following programs:

(a) 

````c
# include <stdio.h>
int main( )
{
    int num[ 26 ], temp ;
    num[ 0 ] = 100 ;
    num[ 25 ] = 200 ;
    temp = num[ 25 ] ;
    num[ 25 ] = num[ 0 ] ;
    num[ 0 ] = temp ;
    printf ( "%d %d\n", num[ 0 ], num[ 25 ] ) ;
    return 0 ;
}
````

````
200 100

````

(b)

````c
# include <stdio.h>
int main( )
{
    int array[ 26 ], i ;
    for ( i = 0 ; i <= 25 ; i++ )
    {
        array[ i ] = 'A' + i ;
        printf ( "%d %c\n", array[ i ], array[ i ] ) ;
    }
    return 0 ;
}
````

````
65 A
66 B
...
...
...
90 Z
````

(c)

````c
# include <stdio.h>
int main( )
{
    int sub[ 50 ], i ;
    for ( i = 0 ; i <= 48 ; i++ ) ;
    {
	    sub[ i ] = i ;
    	printf ( "%d\n", sub[ i ] ) ;
    }
return 0 ;
}
````

````
49

````

