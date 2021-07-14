#include<stdio.h>
#include<stdlib.h>
#define n 5
int main()
{
    int queue[n],choice=1,front=0,rear=0,i,j=1,x=n;
    printf("Queue using Array \n");
    printf("1.Insertion \n");
    printf("2.Deletion \n");
    printf("3.Display \n");
    while(choice)
    {
        printf("\nEnter the Choice:");
        scanf("%d",&choice);
        switch(choice)
        {
        case 1:
            if(rear==x)
                printf("\n Queue is Full");
            else
            {
                printf("\n Enter no %d:",j++);
                scanf("%d",&queue[rear++]);
            }
            break;
        case 2:
            if(front==rear)
            {
                printf("\n Queue is empty");
            }
            else
            {
                printf("\n Deleted Element is %d",queue[front++]);
                x++;
            }
            break;
        case 3:
            printf("\nQueue Elements are:\n ");
            if(front==rear)
                printf("\n Queue is Empty");
            else
            {
                for(i=front; i<rear; i++)
                {
                    printf("%d",queue[i]);
                    printf("\n");
                }
                break;
            }
        }
    }
}
