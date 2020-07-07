# [C] Write a menu driven program which has following options:

<ol>
	<li>Factorial of a number</li>
    <li>Prime or not</li>
    <li>Odd or even</li>
    <li>Exit</li>
</ol>

Once a menu item is selected the appropriate action should be taken and once this action is finished, the menu should reappear. Unless the user selects the ‘Exit’ option the program should continue to run.

Hint: Make use of an infinite **while** and a **switch** statement.

````c
#include<stdio.h>
int main(){
    int a, n;
    while( 1 ){
        printf("\n1. Factorial of a number\n2. Prime or not\n3. Odd or even\n4. Exit\n");
        printf("Enter choice : ");
        scanf("%d", &a);
        switch( a ){

        case 1 : printf("Enter number : ");
                 scanf("%d",&n);
                 int fact = 1;
                 while(n > 0){
                     fact = fact*n;
                     n--;
                 }
                 printf("Factorial is : %d\n",fact);
                 break;

        case 2 : printf("Enter number : ");
                 scanf("%d",&n);
                 int i;
                 for(i=2;i<n/2;i++){
                     if(n%i==0){
                         printf("Not Prime\n");
                         break;
                     }
                 }
                 if(n==i){
                     printf("Prime\n",n);
                 }
                 break;

        case 3 : printf("Enter number : ");
                 scanf("%d",&n);
                 if(n%2==0)
                     printf("Even\n");
                 else
                     printf("Odd\n");
                 break;

        case 4 : exit(1);
                 break;

        default : printf("Wrong choice\n");
                  break;
        }
    }
    return 0;
}
````

