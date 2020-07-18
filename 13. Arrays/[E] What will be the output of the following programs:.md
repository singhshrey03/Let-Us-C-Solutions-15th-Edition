# [E] What will be the output of the following programs:

(a) 

````c
# include <stdio.h>
int main()
{
    int b[ ] = { 10, 20, 30, 40, 50 } ;
    int i ;
    for ( i = 0 ; i <= 4 ; i++ )
    	printf ( "%d\n", *( b + i ) ) ;
    return 0 ;
}
````

````
10
20
30
40
50

````

(b)

````c
# include <stdio.h>
int main( )
{
    int b[ ] = { 0, 20, 0, 40, 5 } ;
    int i, *k ;
    k = b ;
    for ( i = 0 ; i <= 4 ; i++ )
    {
	    printf ( "%d\n", *k ) ;
    	k++ ;
    }
    return 0 ;
}
````

````
0
20
0
40
5

````

(c)

````c
# include <stdio.h>
void change ( int *, int ) ;
int main( )
{
    int a[ ] = { 2, 4, 6, 8, 10 } ;
    int i ;
    change ( a, 5 ) ;
    for ( i = 0 ; i <= 4 ; i++ )
	    printf ( "%d\n", a[ i ] ) ;
    return 0 ;
}
void change ( int *b, int n )
{
    int i ;
    for ( i = 0 ; i < n ; i++ )
	    *( b + i ) = *( b + i ) + 5 ;
}
````

````
7
9
11
13
15

````

(d)

````c
# include <stdio.h>
int main( )
{
    static int a[ 5 ] ;
    int i ;
    for ( i = 0 ; i <= 4 ; i++ )
	    printf ( "%d\n", a[ i ] ) ;
    return 0 ;
}
````

````
0
0
0
0
0

````

(e)

````c
# include <stdio.h>
int main( )
{
    int a[ 5 ] = { 5, 1, 15, 20, 25 } ;
    int i, j, k = 1, m ;
    i = ++a[ 1 ] ;
    j = a[ 1 ]++ ;
    m = a[ i++ ] ;
    printf ( "%d %d %d\n", i, j, m ) ;
}
````

````
3 2 15
````

