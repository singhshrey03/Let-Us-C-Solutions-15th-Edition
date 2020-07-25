# [I] Attempt the following:

(a) Write a program to copy the contents of one array into another in the reverse order.

````c
#include<stdio.h>
int main(){
    int i, rev[10];

    int num[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10} ;

    for(i = 0; i < 10; i++){
        rev[9-i] = num[i];
    }

    for(i = 0; i < 10; i++)
        printf("%d ",rev[i]);

    return 0;
}
````



(b) If an array **arr** contains **n** elements, then write a program to check if **arr[ 0 ] = arr[ n-1 ], arr[ 1 ] = arr[ n - 2 ]** and so on.

````c
#include<stdio.h>
int main(){
    int i;
    int num[] = {1, 2, 3, 4, 5, 6, 4, 2, 3, 1};
    
    for(i = 0; i < 10/2; i++){
        if(num[i] == num[9-i]){
            printf("%d == %d\n", num[i], num[9-i]);
        }
        else{
            printf("%d != %d\n", num[i], num[9-i]);
        }
    }
    return 0;
}
````



(c) Write a program using pointers to find the smallest number in an array of 25 integers.

````c
#include<stdio.h>
int smallest(int *, int);
int main(){
    int i, num[25], min;

    printf("Enter 25 integers:\n");
    for(i = 0; i < 25; i++)
        scanf("%d", &num[i]);

    min = smallest(&num[0], 25);
    printf("Smallest of the 25 integers is %d\n", min);
    return 0;
}

int smallest(int *a, int size){
    int small, i;
    small = a[0];
    for(i = 0; i < size; i++){
        if(a[i] < small){
            small = a[i];
        }
    }
    return small;
}
````



(d) Write a program which performs the following tasks:

<ul>
    <li>Initialize an integer array of 10 elements in main( )</li>
	<li>Pass the entire array to a function modify( )</li>
	<li>In modify( ) multiply each element of array by 3</li>
	<li>Return the control to main( ) and print the new array elements in main( )</li>
</ul>

````c
#include<stdio.h>
void modify (int *, int);
int main(){
    int i, num[10];

    printf("Enter 10 integers:\n");

    for(i = 0; i < 10; i++)
        scanf("%d", &num[i]);

    modify(&num[0], 10);

    for(i = 0; i < 10; i++)
        printf("%d\n", num[i]);

    return 0;
}

void modify(int *a, int size){
    int  i;
    for(i = 0; i < size; i++){
        a[i] = a[i]*3;
    }
}
````

