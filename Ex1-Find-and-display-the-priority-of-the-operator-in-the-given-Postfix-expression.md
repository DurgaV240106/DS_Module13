# EX 1 Display operator precedence in the infix expression.
## DATE:
## AIM:
To write a C program to find and display the priority of the operator in the given Postfix expression

## Algorithm
1.Start the program. 
2. Define the priority() function to return the priority of operators. 
3. Initialize the string containing operators and operands. 
4. Loop through each character in the string. 
5. For each operator, call the priority() function to determine its priority. 
6. Print the operator and its corresponding priority level.
7. End. 

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Durga V
RegisterNumber:  212223230052
*/


#include <stdio.h>
#include<string.h>

int main()
{
   int i,j;
   char ch[100]="100 200 + 2 / 5 * 7 |";
   
   for(i=0;i<strlen(ch);i++)
   {
   if(ch[i]=='+'||
   ch[i]=='-'||
   ch[i]=='*'||
   ch[i]=='/'||
   ch[i]=='%'||
   ch[i]=='^'||
   ch[i]=='&'||
   ch[i]=='|')
       {
       j=priority(ch[i]);
       switch(j)
       {
           case 1:
             printf("%c  ----> ",ch[i]);
           printf("Lowest Priority\n");
             break;
            case 2:
             printf("%c  ----> ",ch[i]);
           printf("Second Lowest Priority\n");
             break;
            case 3:
             printf("%c  ----> ",ch[i]);
           printf("Second Highest Priority\n"); 
             break;
            case 4:
             printf("%c  ----> ",ch[i]);
           printf("Highest Priority\n");
             break;
       }
       }
   }
   
    return 0;
}


```

## Output:
![image](https://github.com/user-attachments/assets/74527340-360b-4160-9a93-e06acba1a904)



## Result:
Thus the C program to find and display the priority of the operator in the given Postfix expression is implemented successfully
