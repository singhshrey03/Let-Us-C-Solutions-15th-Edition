# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int i = 1 ;
    while ( i <= 10 ) ;
    {
    	printf ( "%d\n", i ) ;
    	i++ ;
    }
    return 0 ;
}
````

````

````

NOTE : The above code does not return any output. Since the `while` loop is terminated by a semicolon `;`.

(b)

````c
# include <stdio.h>
int main( )
{
    int x = 4, y, z ;
    y = --x ;
    z = x-- ;
    printf ( "%d %d %d\n", x, y, z ) ;
    return 0 ;
}
````

````
2 3 3

````

(c)

````c
# include <stdio.h>
int main( )
{
    int x = 4, y = 3, z ;
    z = x-- - y ;
    printf ( "%d %d %d\n", x, y, z ) ;
    return 0 ;
}
````

````
3 3 1

````

(d)

````c
# include <stdio.h>
int main( )
{
	while ( 'a' < 'b' )
		printf ( "malayalam is a palindrome\n" ) ;
	return 0 ;
}
````

````
malayalam is a palindrome
````

NOTE : The above output is printed `indefinite` times.

(e)

````c
# include <stdio.h>
int main( )
{
    int i ;
    while ( i = 10 )
    {
        printf ( "%d\n", i ) ;
        i = i + 1 ;
    }
    return 0 ;
}
````

````
10
````

NOTE : The above output is printed `indefinite` times.

(f)

````c
# include <stdio.h>
int main( )
{
    float x = 1.1 ;
    while ( x == 1.1 )
    {
        printf ( "%f\n", x ) ;
        x = x – 0.1 ;
    }
    return 0 ;
}
````

````

````

NOTE : The above code does not return any output. Instead use `while ( x == 1.1f )`.

