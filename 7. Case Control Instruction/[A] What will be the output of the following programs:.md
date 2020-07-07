# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    char suite = 3 ;
    switch ( suite )
    {
        case 1 :
        	printf ( "Diamond\n" ) ;
        case 2 :
    	    printf ( "Spade\n" ) ;
        default :
	        printf ( "Heart\n" ) ;
    }
    printf ( "I thought one wears a suite\n" ) ;
    return 0 ;
}
````

````
Heart
I thought one wears a suite

````

(b)

````c
# include <stdio.h>
int main( )
{
    int c = 3 ;
    switch ( c )
    {
        case '3' :
        	printf ( "You never win the silver prize\n" ) ;
        	break ;
        case 3 :
        	printf ( "You always lose the gold prize\n" ) ;
        	break ;
        default :
        	printf ( "Of course provided you win a prize\n" ) ;
        }
    return 0 ;
}
````

````
You always lose the gold prize

````

(c)

````c
# include <stdio.h>
int main( )
{
    int i = 3 ;
    switch ( i )
    {
        case 0 :
        	printf ( "Customers are dicey\n" ) ;
        case 1 + 0 :
        	printf ( "Markets are pricey\n" ) ;
        case 4 / 2 :
        	printf ( "Investors are moody\n" ) ;
        case 8 % 5 :
        	printf ( "At least employees are good\n" ) ;
    }
    return 0 ;
}
````

````
At least employees are good

````

(d)

````c
# include <stdio.h>
int main( )
{
    int k ;
    float j = 2.0 ;
    switch ( k = j + 1 )
    {
        case 3 :
        	printf ( "Trapped\n" ) ;
        	break ;
        default :
        	printf ( "Caught!\n" ) ;
    }
    return 0 ;
}
````

````
Trapped

````

(e)

````c
# include <stdio.h>
int main( )
{
    int ch = 'a' + 'b' ;
    switch ( ch )
    {
        case 'a' :
        case 'b' :
        	printf ( "You entered b\n" ) ;
        case 'A' :
        	printf ( "a as in ashar\n" ) ;
        case 'b' + 'a' :
        	printf ( "You entered a and b\n" ) ;
    }
    return 0 ;
}
````

````
You entered a and b

````

(f)

````c
# include <stdio.h>
int main( )
{
    int i = 1 ;
    switch ( i - 2 )
    {
        case -1 :
	        printf ( "Feeding fish\n" ) ;
        case 0 :
    	    printf ( "Weeding grass\n" ) ;
        case 1 :
        	printf ( "Mending roof\n" ) ;
        default :
        	printf ( "Just to survive\n" ) ;
    }
    return 0 ;
}
````

````
Feeding fish
Weeding grass
Mending roof
Just to survive

````

NOTE : Every case below `case -1 :` gets printed because we haven't used `break` statement.

