# DS-2
DS code
#include<stdio.h>
#define max 20
int que[max];
int r=-1,f=0,i,ch;
int enqueue()
{
     if(r==max-1)
        {
            printf("\nQueue is full!!\n");
        }
     else
        {
            printf("\nenter element to be inserted: \n");
            scanf("%d",&que[r+1]);
            r++;
        }
        return 0;
}
int dequeue()
{
     if(r==f-1)
     {
        printf("\nqueue is empty\n");
     }
     else
     {
        printf("\n%d is deleted\n", que[f]);
        f++;
     }
     return 0;
}
int display()
{
    printf("\nelements of queue\n");
    for(i=f;i<=r;i++)
        {
            printf("\n%d\n",que[i]);
        }
        return 0;
}
int main()
{
    do
    {
        printf("\n--------------QUEUE-------------\n");
        printf("\nEnter choice\n1.enqueue\n2.dequeue\n3.display\n4.quit:\n");
        printf("\n---------------------------\n");
        scanf("%d",&ch);
        switch(ch)
        {
        case 1:
            {
               enqueue();
               break;
            }
        case 2:
            {
                dequeue();
                break;
            }
        case 3:
            {
                display();
                break;
            }
        }
    }
    while(ch!=4);
    printf("\nExiting!!!");
    return 0;
}

