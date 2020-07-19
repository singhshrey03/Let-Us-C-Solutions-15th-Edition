# [D] Attempt the following:

(a) Twenty-five numbers are entered from the keyboard into an array. The number to be searched is entered through the keyboard by the user. Write a program to find if the number to be searched is present in the array and if it is present, display the number of times it appears in the array.

````c
#include<stdio.h>
int search(int *, int , int);
int main(){
    int i, arr[25], num, count;
    printf("Enter 25 numbers in the array :\n");
    for(i = 0; i < 25; i++){
        scanf("%d", &arr[i]);
    }
    printf("Numbers have been added successfully\n");
    printf("Enter the number to be searched: ");
    scanf("%d", &num);

    count = search(arr, 25, num);

    if(count == 0)
        printf("%d does not appear in the array.\n", num);
    else
        printf("%d appeard %d times in the array.\n", num, count);

    return 0;
}

int search(int *a, int size, int number){
    int c, j;
    for(j = 0; j < size; j++){
        if(*a == number){
            c++;
        }
        a++;
    }
    return c;
}
````

