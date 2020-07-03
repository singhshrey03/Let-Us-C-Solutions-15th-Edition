# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int a = 300, b, c ;
    if ( a >= 400 )
    	b = 300 ;
    c = 200 ;
    printf ( "%d %d\n", b, c ) ;
    return 0 ;
}
````

````
'garbage value' 200

````

NOTE : `b` will contain a `garbage value`since the condition `a>=400` is `False`.

(b)

````c
# include <stdio.h>
int main( )
{
    int a = 500, b, c ;
    if ( a >= 400 )
    	b = 300 ;
    c = 200 ;
    printf ( "%d %d\n", b, c ) ;
    return 0 ;
}
````

````
300 200

````

(c)

````c
# include <stdio.h>
int main( )
{
    int x = 10, y = 20 ;
    if ( x == y ) ;
    	printf ( "%d %d\n", x, y ) ;
    return 0 ;
}
````

````

````

NOTE : The above code does not return any output since `x == y` is `False`.

(d)

````c
# include <stdio.h>
int main( )
{
    int x = 3 ;
    float y = 3.0 ;
    if ( x == y )
    	printf ( "x and y are equal\n" ) ;
    else
    	printf ( "x and y are not equal\n" ) ;
    return 0 ;
}
````

````
x and y are equal

````

(e)

````c
# include <stdio.h>
int main( )
{
    int x = 3, y, z ;
    y = x = 10 ;
    z = x < 10 ;
    printf ( "x = %d y = %d z = %d\n", x, y, z ) ;
    return 0 ;
}
````

````
x = 10 y = 10 z = 0

````

(f)

````c
# include <stdio.h>
int main( )
{
    int i = 65 ;
    char j = ’A’ ;
    if ( i == j )
    	printf ( "C is WOW\n" ) ;
    else
    	printf ( "C is a headache\n" ) ;
    return 0 ;
}
````

````
C is WOW

````

NOTE : ASCII value of `A` is `65`. Hence, `i == j` is `True`.
