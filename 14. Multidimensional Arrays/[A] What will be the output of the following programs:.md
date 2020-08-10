# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int n[ 3 ][ 3 ] = {
                        2, 4, 3, 
                        6, 8, 5, 
                        3, 5, 1 
                        } ;
    printf ( "%d %d %d\n", *n, n[ 3 ][ 3 ], n[ 2 ][ 2 ] ) ;
    return 0 ;
}
````

````
[base address of n] [garbage value] 1

````

(b)

````c
# include <stdio.h>
int main( )
{
    int n[ 3 ][ 3 ] = {
                        2, 4, 3,
                        6, 8, 5,
                        3, 5, 1
                        } ;
    int i, *ptr ;
    ptr = n ;
    for ( i = 0 ; i <= 8 ; i++ )
	    printf ( "%d\n", *( ptr + i ) ) ;
    return 0 ;
}
````

````
2
4
3
6
8
5
3
5
1

````

(c)

````c
# include <stdio.h>
int main( )
{
    int n[ 3 ][ 3 ] = {
                        2, 4, 3,
                        6, 8, 5,
                        3, 5, 1
                        } ;
    int i, j ;
    for ( i = 0 ; i <= 2 ; i++ )
	    for ( j = 0 ; j <= 2 ; j++ )
    		printf ( "%d %d\n", n[ i ][ j ], *( *( n + i ) + j ) ) ;
    return 0 ;
}
````

````
2 2
4 4
3 3
6 6
8 8
5 5
3 3
5 5
1 1

````

