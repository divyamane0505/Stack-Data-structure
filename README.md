#include<stdio.h>
#include<stdlib.h>
#define SIZE 5

void push();
void pop();
int stack[SIZE];
int top=-1;

int main()
{
    int choice;
     while(1)
    {
     
	  printf("\nSelect stack operation\n1.Push\n2.Pop\n3.Exit\n");
       scanf("%d",&choice);   
      switch(choice)
       {
    
	      case 1:
           push();
           break;
          case 2:
           pop();
           break;
          case 3:
           exit(0);
         default:
           printf("Enter correct choice\n");
       }
    }
    return 0;
}

void push()
{
  int element;
  if(top==SIZE-1)
  {
    printf("stack is full");
  }
  else
   {
       top++;
       printf("Enter element for pushing\n");
       scanf("%d",&element);
       stack[top]=element;
    }
}

void pop()
{
  if(top==-1)
  {
  printf("stack is empty\n");
  }
else
   {
     printf("%d is popped",stack[top]);
     top--;
    }
  }
}
