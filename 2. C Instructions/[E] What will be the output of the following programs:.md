# [E] What will be the output of the following programs:

(a) 

```c

#include <stdio.h>
int main( )
{
	int i = 2, j = 3, k, l ;
	float a, b ;
	k = i / j * j ;
	l = j / i * i ;
	a = i / j * j ;
	b = j / i * i ;
	printf ( "%d %d %f %f\n", k, l, a, b ) ;
    return 0;
}
```

```` 
0 2 0.000000 2.000000

````

(b)

````c
#include <stdio.h>
int main( )
{
    int a, b, c, d ;
    a = 2 % 5 ;
    b = -2 % 5 ;
    c = 2 % -5 ;
    d = -2 % -5 ;
    printf ( "a = %d b = %d c = %d d = %d\n", a, b, c, d ) ;
    return 0;
}
````

````
a = 2 b = -2 c = 2 d = -2

````

(c)

````c
#include <stdio.h>
int main( )
{
    float a = 5, b = 2 ;
    int c, d ;
    c = a % b ;
    d = a / 2 ;
    printf ( "%d\n", d ) ;
    return 0 ;
}
````

````
2

````

NOTE : The statement `c = a % b;` may result in error since `a`  and `b` are `float` variables.

Instead use, `c = fmod(a, b);` from the header file `math.h`.

(d)

````c
#include <stdio.h>
int main()
{
    printf ( "nn \n\n nn\n" ) ;
    printf ( "nn /n/n nn/n" ) ;
    return 0 ;
}
````

````
nn 

 nn
nn /n/n nn/n
````

(e)

````c
#include <stdio.h>
int main( )
{
    int a, b ;
    printf ( "Enter values of a and b" ) ;
    scanf ( " %d %d ", &a, &b ) ;
    printf ( "a = %d b = %d", a, b ) ;
    return 0 ;
}
````

````
Enter values of a and b 
````

NOTE : The above code will return the values of `a` and `b` as provided by the user.
