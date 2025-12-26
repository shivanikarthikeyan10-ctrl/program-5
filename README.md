Program-5-a
C-Module 5
EX_NO-05)a)-Pointers
Date: 26/12/25
Name: SHIVANI K
Register Number:25013585


AIM:

Write a C program to check whether the number 8887 is even number or odd number using pointers.

ALGORITHM:

Start the program.

Declare an integer variable to store the input number and an integer pointer variable.

Read the integer value from the user using scanf.

Assign the address of the integer variable to the pointer.

Check if the value pointed to by the pointer is even using the modulus operator (%):

a. If it is even, print " is even."

b. Otherwise, print " is odd."

End the program.

PROGRAM:

#include<stdio.h>
int main()
{
    int num,*p1;
    scanf("%d",&num);
    p1=&num;
    if(*p1%2==0)
    printf("%d is even.",num);
    else
    printf("%d is odd.",num);
}


OUTPUT:

Screenshot 2025-10-20 083200

RESULT:

Thus the program to check whether the number 8887 is even number or odd number using pointers has been executed successfully

Program-5-b
C-Module 5
EX_NO-05)b)-Functions & Storage Classes
Date: 26/12/25
Name: SHIVANI K
Register Number: 25013585


AIM:

write a program to print even numbers in given range using recursion

ALGORITHM:

Start the program.

Define a function named even that takes two integer arguments: st (start) and end.

Inside the function:

a. If st is greater than end, return (stop recursion).

b. If st is even (st % 2 == 0), print the value of st.

c. Recursively call the even function with st + 1 and end as arguments.

In the main function:

a. Declare two integer variables st and end.

b. Read the values of st and end from the user using scanf.

c. Print a message indicating the range of even numbers.

d. Call the even function with st and end as arguments.

End the program.

PROGRAM:

#include<stdio.h>
void even(int st,int end)
{
    if(st>end)
    return;
    if(st%2==0)
    printf(" %d",st);
    even(st+1,end);
}
int main()
{
    int st,end;
    scanf("%d%d",&st,&end);
    printf("Even Numbers from %d to %d are:",st,end);
    even(st,end);
}


OUTPUT:


Screenshot 2025-10-20 083757

RESULT:

Thus the program to print even numbers in given range using recursion has been executed successfully


Program-5-c
C-Module 5
EX_NO-05)c)-Arrays & Its Operations
Date: 26/12/25
Name: SHIVANI K
Register Number:25013585


AIM:

Write a C Program to displays the lower triangular and its sum of a matrix

ALGORITHM:

Start the program.

Declare two integer variables to store the number of rows and columns.

Read the values of rows and columns from the user using scanf.

Declare a two-dimensional array with the given number of rows and columns.

Print a message "matrix is".

Use nested for loops to read elements into the matrix:

a. Outer loop iterates over rows.

b. Inner loop iterates over columns.

c. Read each element using scanf.

Use nested for loops to display the matrix in proper format:

a. Print each element followed by a space.

b. Move to a new line after each row.

Initialize a variable sum to 0.

Use nested for loops to find and print elements of the lower triangle:

a. Check if the current element position satisfies the lower triangle condition (i == 3) or (i == 2 && j != 3) or (i == 1 && j == 1).

b. If true, print the element and add it to sum.

After processing all elements, print the total sum of the lower triangle.

End the program.


PROGRAM:

#include<stdio.h>
int main()
{
    int row,col;
    scanf("%d%d",&row,&col);
    int arr[row][col];
    printf("matrix is\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        scanf("%d",&arr[i][j]);
    }
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        printf("%d ",arr[i][j]);
        printf("\n");
    }
    int sum=0;
    printf("\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        {
            if(i==3||(i==2&&j!=3)||(i==1&&j==1))
            {
                printf("%d ",arr[i][j]);
                sum+=arr[i][j];
            }}
            printf("\n");
    }
    printf("Sum of Lower Triangle is %d",sum);
}


OUTPUT:


Screenshot 2025-10-20 084241

RESULT:

Thus the program to displays the lower triangular and its sum of a matrix has been executed successfully


Program-5-d
C-Module 5
EX_NO-05)e)-Strings
Date: 26/12/25
Name: SHIVANI K
Register Number:25013585


AIM:

Write a program in C to replace the spaces of a string with a specific character.

ALGORITHM:

Start the program.

Declare a character array to store the input string and a character variable to store the replacement character.

Read a line of text from the user using fgets.

Read a single character from the user using scanf.

Use a for loop to iterate through each character in the string until the null character ('\0') is reached:

a. If the current character is a space (' '), replace it with the given character.

After the loop, print the updated string along with a message showing the replacement character.

End the program.


PROGRAM:

#include<stdio.h>
#include<string.h>
#include<ctype.h>
int main()
{
    char str[30];
    fgets(str,sizeof(str),stdin);
    char ch;
    scanf("%c",&ch);
    for(int i=0;str[i]!='\0';i++)
    {
        if(str[i]==' ')
        str[i]=ch;
    }
    printf("After replacing the space with  %c the new string is :\n%s",ch,str);
}


OUTPUT:

Screenshot 2025-10-20 085227

RESULT:

Thus the program to replace the spaces of a string with a specific character has been executed successfully

Program-5-e
C-Module 5
EX_NO-05)e)-Arrays
Date: 26/12/25
Name: SHIVANI K
Register Number:25013585


AIM:

Write a C Program to displays the lower triangular of a matrix

ALGORITHM:

Start the program.

Declare two integer variables to store the number of rows and columns.

Read the values of rows and columns from the user using scanf.

Declare a two-dimensional array with the given number of rows and columns.

Use nested for loops to read elements into the matrix:

a. Outer loop iterates over rows.

b. Inner loop iterates over columns.

c. Read each element using scanf.

Print the message "matrix is".

Use nested for loops to display the entire matrix:

a. Print each element followed by a space.

b. Move to a new line after each row.

Use nested for loops to display specific elements based on conditions:

a. If the current position satisfies (i==1 && j==1) or (i==2 && j!=3) or (i==3), print the element.

b. Move to a new line after each row.

End the program.


PROGRAM:

#include<stdio.h>
int main()
{
    int row,col;
    scanf("%d%d",&row,&col);
    int arr[row][col];
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        scanf("%d",&arr[i][j]);
    }
    printf("matrix is\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        {
            printf("%d ",arr[i][j]);
        }
        printf("\n");
    }
    printf("\n");
    for(int i=1;i<=row;i++)
    {
        for(int j=1;j<=col;j++)
        {
            if((i==1&&j==1)||(i==2&&j!=3)||i==3)
            printf("%d ",arr[i][j]);
        }
        printf("\n");
    }
}


OUTPUT:

Screenshot 2025-10-20 090503

RESULT:

Thus the program to displays the lower triangular of a matrix has been executed successfully
