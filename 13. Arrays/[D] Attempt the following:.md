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

(b) Implement the Selection Sort, Bubble Sort and Insertion sort algorithms on a set of 25 numbers.

<ul>
    <li>Selection Sort</li>
    <li>Bubble Sort</li>
    <li>Insertion Sort</li>
</ul>



![Selection-Sort](https://github.com/singhshrey/Let-Us-C-Solutions-15th-Edition/blob/master/13.%20Arrays/selection_sort.PNG)


````c
// Selection Sort

#include<stdio.h>

void selection_sort(int *, int);
int find_min_pos(int *a, int, int);

int main(){
    int i, arr[25];
    printf("Enter 25 numbers:\n");

    for(i=0;i<25;i++)
        scanf("%d",&arr[i]);
    printf("Numbers added successfully\n");

    selection_sort(&arr[0], 25);

    printf("Sorted array is :\n");
    for(i=0;i<25;i++)
        printf("%d\n",arr[i]);
    return 0;
}

void selection_sort(int *a, int size){
    int i, min_pos, temp, j;
    for(i=0; i<size; i++){
        min_pos = find_min_pos(&a[0], i, size);
        temp = a[i];
        a[i] = a[min_pos];
        a[min_pos] = temp;
    }
}

int find_min_pos(int *a, int x, int size){
    int i, min, pos;
    min = a[x];
    for(i=x; i<size; i++){
        if(a[i] <= min){
            min = a[i];
            pos = i;
        }
    }
    return pos;
}
````

![Bubble-Sort](https://github.com/singhshrey/Let-Us-C-Solutions-15th-Edition/blob/master/13.%20Arrays/bubble_sort.PNG)


````c
// Bubble Sort

#include<stdio.h>

void bubble_sort(int *, int);

int main(){
    int i, arr[25];

    printf("Enter 25 numbers:\n");

    for(i=0;i<25;i++)
        scanf("%d",&arr[i]);
    printf("Numbers added successfully\n");

    bubble_sort(&arr[0], 25);

    printf("Sorted array is :\n");
    for(i=0;i<25;i++)
        printf("%d\n",arr[i]);

    return 0;
}

void bubble_sort(int *a, int size){
    int i, j, k, temp;
    for(i=0;i<size;i++){
        for(j=0; j<size-1-i; j++){
            if(a[j]>a[j+1]){
                temp = a[j+1];
                a[j+1] = a[j];
                a[j] = temp;
            }
        }
    }
}
````

![Insertion-Sort](https://github.com/singhshrey/Let-Us-C-Solutions-15th-Edition/blob/master/13.%20Arrays/insertion_sort.PNG)


````c
// Insertion Sort

#include<stdio.h>

void insertion_sort(int *, int);

int main(){
    int i, arr[25];

    printf("Enter 25 numbers:\n");

    for(i=0;i<25;i++)
        scanf("%d",&arr[i]);
    printf("Numbers added successfully\n");

    insertion_sort(&arr[0], 25);

    printf("Sorted array is :\n");
    for(i=0;i<25;i++)
        printf("%d\n",arr[i]);

    return 0;
}

void insertion_sort(int *a, int size){
    int i, j, k, temp;
    for(i=0;i<size;i++){
        for(j=0; j<i;j++){
            if(a[j]>a[i]){
                temp = a[j];
                a[j] = a[i];
                a[i] = temp;
            }
        }
    }
}
````

(c) Implement in a program the following procedure to generate prime numbers from 1 to 100. This procedure is called sieve of Eratosthenes.

Step 1: Fill an array num[ 100 ] with numbers from 1 to 100.

Step 2: Starting with the second entry in the array, set all its multiples to zero.

Step 3: Proceed to the next non-zero element and set all its multiples to zero.

Step 4: Repeat Step 3 till you have set up the multiples of all the non-zero elements to zero.

Step 5: At the conclusion of Step 4, all the non-zero entries left in the array would be prime numbers, so print out these numbers.

````c
#include<stdio.h>
int main(){
    int i, j, k, step, num[100];

    for(i=0;i<100;i++)
        num[i] = i+1;

    for(i=1;i<100;i++){

        if(num[i] != 0){
            
            step = num[i];
            k = num[i]*2-1;

            for(j=k;j<100;j+=step){
                num[j] = 0;
            }
        }
    }

    for(i=1;i<100;i++){
        if(num[i] != 0){
            printf("%d  ",num[i]);
        }
    }

    return 0;
}
````

(d) Twenty-five numbers are entered from the keyboard into an array. Write a program to find out how many of them are positive, how many are negative, how many are even and how many odd.

````c
#include<stdio.h>
int main(){
    int i, num[25], pos, neg, even, odd;
    pos = 0;
    neg = 0;
    even = 0;
    odd = 0;

    printf("Enter 25 numbers:\n");

    for(i = 0; i < 25; i++)
        scanf("%d", &num[i]);

    for(i = 0; i < 25; i++){

        if(num[i] > 0)
            pos++;
        else
            neg++;

        if(num[i] % 2 == 0)
            even++;
        else
            odd++;
    }

    printf("Positive %d\nNegative %d\nEven %d\nOdd %d\n",pos, neg, even, odd);
    
    return 0;
}
````

(e) Write a program that interchanges the odd and even elements of an array.

````c
#include <stdio.h>
int main()
{
    int num[] = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
    int i, t;

    for(i = 0; i < 10; i+=2){
        t = num[i];
        num[i] = num[i+1];
        num[i+1] = t;
    }

    for(i = 0; i < 10; i++){
        printf("%d ", num[i]);
    }
    return 0;
}
````

