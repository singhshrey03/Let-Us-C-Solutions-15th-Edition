# [B] Point out the errors, if any, in the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int suite = 1 ;
    switch ( suite ) ;
    {
        case 0 ;
        	printf ( "Club\n" ) ;
        case 1 ;
        	printf ( "Diamond\n" ) ;
    }
    return 0 ;
}
````

Semicolon `;` must **not** be used after the `switch` statement. Use `:` instead of `;` at the end of a `case` statement.

(b)

````c
# include <stdio.h>
int main( )
{
    int temp ;
    scanf ( "%d", &temp ) ;
    switch ( temp )
    {
        case ( temp <= 20 ) :
        	printf ( "Ooooooohhhh! Damn cool!\n" ) ;
        case ( temp > 20 && temp <= 30 ) :
        	printf ( "Rain rain here again!\n" ) ;
        case ( temp > 30 && temp <= 40 ) :
        	printf ( "Wish I am on Everest\n" ) ;
        default :
    	    printf ( "Good old nagpur weather\n" ) ;
    }
    return 0 ;
}
````

Cases can never have a variable expression. Also, **Relational Operators** are not allowed in switch case.

(c)

````c
# include <stdio.h>
int main( )
{
    float a = 3.5 ;
    switch ( a )
    {
        case 0.5 :
        	printf ( "The art of C\n" ) ; break ;
        case 1.5 :
        	printf ( "The spirit of C\n" ) ; break ;
        case 2.5 :
        	printf ( "See through C\n" ) ; break ;
        case 3.5 :
        	printf ( "Simply c\n" ) ;
    }
    return 0 ;
}
````

A float expression cannot be tested using a `switch`.

(d)

````c
# include <stdio.h>
int main( )
{
    int a = 3, b = 4, c ;
    c = b – a ;
    switch ( c )
    {
    	case 1 || 2 :
    		printf ( "God give me a chance to change things\n" ) ;
    		break ;
    	case a || b :
    		printf ( "God give me a chance to run my show\n" ) ;
		    break ;
    }
    return 0 ;
}
````

Cases can never have a variable expression. Also, **Logical Operators** cannot be used in switch case.

