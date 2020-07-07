# [D] Write a program to find the grace marks for a student using switch. The user should enter the class obtained by the student and the number of subjects he has failed in. Use the following logic:

<ul>
    <li>If the student gets first class and the number of subjects he failed in is greater than 3, then he does not get any grace. Otherwise the grace is of 5 marks per subject.</li>
    <li>If the student gets second class and the number of subjects he failed in is greater than 2, then he does not get any grace. Otherwise the grace is of 4 marks per subject.</li>
    <li>If the student gets third class and the number of subjects he failed in is greater than 1, then he does not get any grace. Otherwise the grace is of 5 marks.</li>
</ul>



````c
#include<stdio.h>
int main(){
    int cls, failed;
    printf("Enter class and subjects failed: ");
    scanf("%d%d",&cls,&failed);
    switch(cls){
        case 1 : if(failed > 3)
                     printf("No Grace");
                 else
                     printf("5 marks grace");
                 break;
        case 2 : if(failed > 2)
                     printf("No Grace");
                 else
                     printf("4 marks grace");
                 break;
        case 3 : if(failed > 1)
                     printf("No Grace");
                 else
                     printf("5 marks grace");
        default : break;
    }
    return 0;
}
````

