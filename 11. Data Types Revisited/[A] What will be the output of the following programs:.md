# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int i ;
    for ( i = 0 ; i <= 50000 ; i++ )
    printf ( "%d\n", i ) ;
    return 0 ;
}
````

````
0
1
2
...
...
50000
````

(b)

````c
# include <stdio.h>
int main( )
{
    float a = 13.5 ;
    double b = 13.5 ;
    printf ( "%f %lf\n", a, b ) ;
    return 0 ;
}
````

````
13.500000 13.500000

````

(c)

````c
# include <stdio.h>
int i = 0 ;
void val( ) ;
int main( )
{
    printf ( "main's i = %d\n", i ) ;
    i++ ;
    val( ) ;
    printf ( "main's i = %d\n", i ) ;
    val( ) ;
    return 0 ;
}
void val( )
{
    i = 100 ;
    printf ( "val's i = %d\n", i ) ;
    i++ ;
}
````

````
main's i = 0
val's i = 100
main's i = 101
val's i = 100
````

(d)

````c
# include <stdio.h>
int f ( int ) ;
int g ( int ) ;
int main( )
{
    int x, y, s = 2 ;
    s *= 3 ;
    y = f ( s ) ;
    x = g ( s ) ;
    printf ( "%d %d %d\n", s, y, x ) ;
    return 0 ;
}
int t = 8 ;
int f ( int a )
{
    a += -5 ;
    t -= 4 ;
    return ( a + t ) ;
}
int g ( int a )
{
    a = 1 ;
    t += a ;
    return ( a + t ) ;
}
````

````
6 5 6

````

(e)

````c
# include <stdio.h>
int main( )
{
    static int count = 5 ;
    printf ( "count = %d\n", count-- ) ;
    if ( count != 0 )
	    main( ) ;
    return 0 ;
}
````

````
count = 5
count = 4
count = 3
count = 2
count = 1

````

(f)

````c
# include <stdio.h>
int g ( int ) ;
int main( )
{
    int i, j ;
    for ( i = 1 ; i < 5 ; i++ )
    {
        j = g ( i ) ;
        printf ( "%d\n", j ) ;
    }
    return 0 ;
}
int g ( int x )
{
    static int v = 1 ;
    int b = 3 ;
    v += x ;
    return ( v + x + b ) ;
}
````

````
6
9
13
18

````

(g)

````c
# include <stdio.h>
int main( )
{
    func( ) ;
    func( ) ;
    return 0 ;
}
void func( )
{
    auto int i = 0 ;
    register int j = 0 ;
    static int k = 0 ;
    i++ ; j++ ; k++ ;
    printf ( "%d % d %d\n", i, j, k ) ;
}
````

````
1 1 1
1 1 2

````

(h)

````c
# include <stdio.h>
int x = 10 ;
int main( )
{
    int x = 20 ;
    {
        int x = 30 ;
        printf ( "%d\n", x ) ;
    }
    printf ( "%d\n", x ) ;
    return 0 ;
}
````

````
30
20

````

