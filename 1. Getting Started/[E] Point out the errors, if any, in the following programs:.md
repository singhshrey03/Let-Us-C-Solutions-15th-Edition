# [E] Point out the errors, if any, in the following programs:

(a)

```
int main( )
{
    int a, float b, int c ;
	a = 25 ; b = 3.24 ; c = a + b * b – 35 ;
}
```

**Statement terminator ( ; )** expected before `float b` and `int c`.

(b)

```
/* Calculation of average
	/* Author: Sanjay */
	/* Place – Whispering Bytes */
*/
#include <stdio.h>
int main( )
{
int a = 35 ; float b = 3.24 ;
printf ( "%d %f %d", a, b + 1.5, 235 ) ;
}
```

Comments cannot be nested.

(c) 

```
#include <stdio.h>
int main( )
{
	int a, b, c ;
	scanf ( "%d %d %d", a, b, c ) :
}
```

Use of **Address of  (&)** operator is must before variables in `scanf()`.

(d) 

```
#include <stdio.h>
int main( )
{
	int m1, m2, m3
	printf ( "Enter values of marks in 3 subjects" )
	scanf ( "%d %d %d", &m1, &m2, &m3 )
	printf ( "You entered %d %d %d", m1, m2, m3 ) ;
}
```

Every C statement must end with a semicolon **( ; )**.
