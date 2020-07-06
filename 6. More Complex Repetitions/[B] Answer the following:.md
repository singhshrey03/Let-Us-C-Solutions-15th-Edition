# [B] Answer the following:

(a) The three parts of the loop expression in the **for** loop are:

````
the initialization expression

the testing expression

the incrementation expression
````

(b) The **break** statement is used to exit from:

````
2.  A for loop
````

(c) A **do-while** loop is useful when we want that the statements within the loop must be executed:

````
2.  At least once
````

(d) In what sequence the initialization, testing and execution of body is done in a **do-while** loop

````
1.  Initialization, execution of body, testing
````

(e) Which of the following is not an infinite loop?

````
3.  int t = 0, f ;
    while ( t )
    {
      f = 1 ;
    }
````

(f) Which keyword is used to take the control to the beginning of the loop?

````
continue
````

(g) How many times the while loop in the following C code will get executed?

````c
# include <stdio.h>
int main( )
{
    int j = 1 ;
    while ( j <= 255 ) ;
    {
      printf ( "%c %d ", j, j ) ;
      j++;
    }
    return 0 ;
}
````

````
Infinite times. Because the while statement is terminated by a semicolon ( ; ) .
````

(h) Which of the following statements is true for the following program?

````c
# include <stdio.h>
int main( )
{
    int x=10, y = 100%90 ;
    for ( i = 1 ; i <= 10 ; i++ ) ;
    if ( x != y ) ;
    	printf ( "x = %d y = %d\n", x, y ) ;
    return 0 ;
}
````

````
2. The program will produce the output x=10 y=10.
3. The ; after the if (x!=y) would not produce an error.
````

(i) Which of the following statement is true about a **for** loop used in a C program?

1. **for** loop works faster than a **while** loop.
2. All things that can be done using a **for** loop can also be done using a **while** loop.
3. **for ( ; ; )** implements an infinite loop.
4. **for** loop can be used if we want statements in a loop to get executed at least once.
5. **for** loop works faster than a **do-while** loop.

````
2. All things that can be done using a for loop can also be done using a while loop.
3. for ( ; ; ) implements an infinite loop.
4. for loop can be used if we want statements in a loop to get executed at least once.
````

