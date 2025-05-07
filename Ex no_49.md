# EX 49 C function to search an element in the doubly linked list.
## DATE: 
## AIM:
To write a C function to search an element in the doubly linked list.

## Algorithm
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
void search(char data)
{
    struct Node *ptr;
    char item=data;
    int i=0,flag;
    ptr = head;
    if(ptr == NULL)
    {
    printf("Empty List\n");
    }
    else
    {
        printf("\nEnter item which you want to search?\n");
        scanf("%d",&item);
        while (ptr!=NULL)
        {
            if(ptr->data == item)
            {
                printf("item %c found at location %d\n",item,i+1);
                flag=0;
            }
            else
            {
               flag=1;
                printf("item not found");    
            }
            i++;
            ptr = ptr -> next;
        }
        if(flag!=0)
        {
            printf("Item not found\n");
        }
    }
}

```

## Output:
![Screenshot 2025-05-07 184002](https://github.com/user-attachments/assets/44d4dd95-682c-4562-ac0b-460a8dbc8d58)



## Result:
Thus the program was executed and the output was verified successfully.
