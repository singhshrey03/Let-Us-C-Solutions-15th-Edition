# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    int i = 0 ;
    for ( ; i ; )
    	printf ( "Here is some mail for you\n" ) ;
    return 0 ;
}
````

````

````

NOTE : The above code does not return any output. Since the testing expression in the `for` loop returns a `False` value i.e. `0` .

(b)

````c
# include <stdio.h>
int main( )
{
    int i ;
    for ( i = 1 ; i <= 5 ; printf ( "%d\n", i ) ) ;
	    i++ ;
    return 0 ;
}
````

````
1
````

NOTE : The above output is printed `indefinite` times.

(c)

````c
# include <stdio.h>
int main( )
{
    int i = 1, j = 1 ;
    for ( ; ; )
    {
    	if ( i > 5 )
    		break ;
    else
	    j += i ;
    printf ( "%d\n", j ) ;
    i += j ;
    return 0 ;
    }
}
````

````
2
5

````

