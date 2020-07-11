# [A] What will be the output of the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    printf ( "C to it that C survives\n" ) ;
    main( ) ;
    return 0 ;
}
````

````
C to it that C survives
````

NOTE : The above output is printed `indefinite` times.

(b)

````c
# include <stdio.h>
int main( )
{
    int i = 0 ;
    i++ ;
    if ( i <= 5 )
    {
        printf ( "C adds wings to your thoughts\n" ) ;
        exit ( 0 ) ;
        main( ) ;
    }
    return 0 ;
}
````

````
C adds wings to your thoughts
````

