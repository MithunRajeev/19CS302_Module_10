# EX 50 C function to delete a node from a Doubly Linked List at the beginning of the list.
## DATE:
## AIM:
To write a C function to delete a node from a Doubly Linked List at the beginning of the list.

## Algorithm:
1. Start. 
2. Define a variables. 
3. Write a function to perform all basic operations. 
4. Read the value using scanf. 
5. Ask the user to make an input. 
6. Print out the answer. 
7. End.   

## Program:
```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;
void delete()
{
    struct Node *ptr;
    if(head == NULL)
    {
        printf("UNDERFLOW\n");
    }
    else if(head->next == NULL)
    {
        head = NULL;
        free(head);
        printf("Node deleted\n");
    }
    else
    {
        ptr = head;
        head = head -> next;
        head -> prev = NULL;
        free(ptr);
        printf("Node deleted\n");
    }
}

```

## Output:
![Screenshot 2025-05-07 185756](https://github.com/user-attachments/assets/8cb07b8b-da58-41ee-b8a5-0dde50ee0eff)


## Result:
Thus the program was executed and the output was verified successfully.
