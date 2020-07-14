# [C] Answer the following:

(1) Why are addresses of functions stored on the stack?

````
This makes the transfer of control easier to the function after the required values are returned from other function. 
````

(2) How do we decide whether a variable should be passed by value or by reference?

````
Call by value: Changes will not be reflected on actual arguments.

Call by reference: Changes will be reflected on actual arguments.
````

(3) Size of a pointer is not dependent on whose address is stored in it. Justify.

````
A pointer is a variable which is meant to hold the address of other variables.
This address happens to be of a fixed size of 4 bytes.
It does not depend on the type of variable whose address is being stored.
````

(4) At times there may be holes in a structure? Why do they exist? How can they be avoided?

````
Hole concept is found in `Structures` in C language where,
the compiler leaves certain holes in the memory alignment when it allocates memory on the page boundaries.
Thats the reason you get the sizeof structure some times greater than the sum of all the fields in the structure.

This can be corrected by using the preprocessor directive, #pragma pack[1]
````

(5) A recursive call should always be subjected to an if. Why? Explain with an example.

````
If recursive call is not subjected to an if, it may fall into an indefinite loop.

int main()
{
    callme();
    ...
    return 0;
}
void rec()
{
    statement 1;
    ...
    rec();
}

In the beginning main() function called rec(), then inside rec() function, it called itself again.
As you can guess this process will keep repeating indefinitely.
So, in a recursive function, there must be a terminating condition to stop the recursion.
````

