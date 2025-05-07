# EX 48 C functions to perform all basic operations in Doubly Linked List.
## DATE:
## AIM:
To write a C functions to perform all basic operations in Doubly Linked List.

## Algorithm:
1. Start. 
2. Define a variables. 
3. Write a function to search an element in the double linked list.. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End
   
## Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head;
void display()
{
    struct Node *ptr;
    ptr = head;
    while(ptr != NULL)
    {
        printf("%c ",ptr->data);
        ptr=ptr->next;
    }
}
void insert(char data)
{
   struct Node *ptr,*temp;
   ptr=(struct Node *)malloc(sizeof(struct Node));
   if(ptr==NULL)
   {
       printf("OVERFLOW\n");
   }
   else
   {
       ptr->data=data;
       if(head==NULL)
       {
           ptr->next=NULL;
           ptr->prev=NULL;
           head=ptr;
       }
       else
       {
          temp=head;
          while(temp->next!=NULL)
          {
              temp=temp->next;
          }
          temp->next=ptr;
          ptr->prev=temp;
          ptr->next=NULL;
        }
    }
}
void search(char data)
{
    struct Node *ptr;
    char item=data;
    int i=0,flag;
    ptr=head;
    if(ptr==NULL)
    {
    printf("Empty List\n");
    }
    else
    {
       while(ptr!=NULL)
        {
            if(ptr->data==item)
            {
                printf("item %c found at location %d\n",item,i+1);
                flag=0;
            }
             else
            {
               flag=1;
            }
            i++;
            ptr=ptr->next;
        }
        if(flag!=0)
        {
            printf("Item not found\n");
        }
    }
}
void delete()
{
    struct Node *ptr;
    if(head==NULL)
    {
        printf("UNDERFLOW\n");
    }
    else if(head->next==NULL)
    {
        head=NULL;
        free(head);
        printf("Node deleted\n");
    }
    else
    {
        ptr=head;
        head=head->next;
        head->prev=NULL;
        free(ptr);
        printf("Node deleted\n");
    }
}
```

## Output:
![Screenshot 2025-05-07 184002](https://github.com/user-attachments/assets/cd0c9256-db31-4815-9dd8-e028a5169640)



## Result:
Thus the program was executed and the output was verified successfully.
