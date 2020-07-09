# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
void display( ) ;
int main( )
{
    printf ( "Learn C\n" ) ;
    display( ) ;
    return 0 ;
}
void display( )
{
    printf ( "Followed by C++, C# and Java!\n" ) ;
    main( ) ;
}
````

````
Learn C
Followed by C++, C# and Java!
````

NOTE : The above output is printed `indefinite` times.

(b)

````c
# include <stdio.h>
int check ( int ) ;
int main( )
{
    int i = 45, c ;
    c = check ( i ) ;
    printf ( "%d\n", c ) ;
    return 0 ;
}
int check ( int ch )
{
    if ( ch >= 45 )
    	return ( 100 ) ;
    else
    	return ( 10 * 10 ) ;
}
````

````
100

````

(c)

````c
# include <stdio.h>
float circle ( int ) ;
int main( )
{
    float area ;
    int radius = 1 ;
    area = circle ( radius ) ;
    printf ( "%f\n", area ) ;
    return 0 ;
}
float circle ( int r )
{
    float a ;
    a = 3.14 * r * r ;
    return ( a ) ;
}
````

````
3.140000

````

(d)

````c
# include <stdio.h>
int main( )
{
    void slogan( ) ;
    int c = 5 ;
    c = slogan( ) ;
    printf ( "%d\n", c ) ;
    return 0 ;
}
void slogan( )
{
	printf ( "Only He men use C!\n" ) ;
}
````

````

````

**Error.** Return type of the function `slogan` is `void`.

