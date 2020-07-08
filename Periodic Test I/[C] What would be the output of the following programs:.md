# [C] What would be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int x = 5, y, z ;
    y = x++ ;
    z = x-- ;
    printf ( "%d %d %d", x, y, z ) ;
    return 0 ;
}
````

````
5 5 6
````

(b)

````c
# include <stdio.h>
int main( )
{
    int i = 65 ;
    char ch = i ;
    printf ( "%d %c", ch, i ) ;
    return 0 ;
}
````

````
65 A
````

(c)

````c
# include <stdio.h>
int main( )
{
    int i, j ;
    for ( i = 1 ; i <= 2 ; i++ )
    {
        for ( j = 1 ; j <= 2 ; j++ )
        {
            if ( i == j )
            	break ;
            printf ( “%d %d”, i, j ) ;
        }
    }
    return 0 ;
}
````

````
2 1
````

(d)

````c
# include <stdio.h>
int main( )
{
    int x = 3, i = 1 ;
    while ( i <=2 )
    {
        printf ( "%d", x *= x + 4 ) ;
        i++ ;
    }
    return 0 ;
}
````

````
21525
````

| i     | x *= x + 4                    |
| ----- | -------------------- |
| i = 1 | 3 * ( 3 + 4) = 21    |
| i = 2 | 21 * ( 21 + 4) = 525 |

(e)

````c
# include <stdio.h>
int main( )
{
    int a, b = 5 ;
    a = !b ;
    b = !a ;
    printf ( "%d %d", a, b ) ;
    return 0 ;
}
````

````
0 1
````

