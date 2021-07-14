#include<stdio.h>
#include<stdlib.h>
#define MAX100
int stack[100];
int top=-1;
void push(int);
int pop();
void peek();
void traverse();
void main()
{
    int choice,n;
    do
    {
        printf("1.push \n");
        printf("2.pop \n");
        printf("3.peek \n");
        printf("4.traverse \n");
        printf("enter your choice \n");
        scanf("%d",&choice);
        switch(choice)
        {
            case 1:printf("enter an element \n");
                   scanf("%d",&n);
                   push(n);
                   break;
            case 2:n=pop();
                if(n==0)
                {
                  printf("stack is underflow \n ");
                }
                else
                {
                    printf("popped element : %d \n",n);
                }
                break;
            case 3:peek();
                break;
            case 4:traverse();
                   break;
        }
    }while(choice!=4);
}
void push(int n)
{
    if(top==100)
    {
        printf("overflow");
    }
    else
    {
        top=top+1;
        stack[top]=n;
        printf("element is pushed \n");
    }
}
int pop()
{
    if(top==-1)
    {
        printf("underflow \n");
    }
    else
    {
        return stack[top--];
    }
}
void peek()
{
    if(top==-1)
    {
        printf("stack is empty \n");
        
    }
    else
    {
        printf("top is : %d \n",stack[top]);
    }
}
void traverse()
{
    if(top==-1)
    {
        printf("stack is empty \n");
    }
    else
    {
        int i;
        printf("stack elements are : \n");
        for(i=top;i>=0;i--)
        {
            printf("%d \n",stack[i]);
        }
    }
}
