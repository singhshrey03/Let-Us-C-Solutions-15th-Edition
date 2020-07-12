# [B] Point out the errors, if any, in the following programs:

(a)

````c
# include <stdio.h>
int main( )
{
    long num ;
    num = 2 ;
    printf ( "%d\n", num ) ;
    return 0 ;
}
````

The format specifier for variable  `num` should be `%ld` instead of `%d` since it is a `long int` variable.

(b)

````c
# include <stdio.h>
int main( )
{
    char ch = 200 ;
    printf ( "%d\n", ch ) ;
    return 0 ;
}
````

The for specifier for variable `ch` should be `%c` instead of `%d` since it is a `char` variable.

(c)

````c
# include <stdio.h>
int main( )
{
    unsigned a = 25 ;
    long unsigned b = 25l ;
    printf ( "%lu %u\n", a, b ) ;
    return 0 ;
}
````

The format specifiers `%lu` and `%u` must be swapped since `a` is `unsigned` and `b` is `long unsigned`.

(d)

````c
# include <stdio.h>
int main( )
{
    long float a = 25.345e454 ;
    unsigned double b = 25 ;
    printf ( "%lf %d\n", a, b ) ;
    return 0 ;
}
````

There is no data type `long float` in C.

(e)

````c
# include <stdio.h>
static int y ;
int main( )
{
    static int z ;
    printf ( "%d %d\n", y, z ) ;
    return 0 ;
}
````

**No error**.

