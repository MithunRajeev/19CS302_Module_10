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
#include <stdio.h>
#include <stdlib.h>
struct Node
{
    char data;
    struct Node* prev;
    struct Node* next;
};
struct Node* head = NULL;
void insert(char value)
{
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node*));
    newNode->data = value;
    newNode->prev = newNode->next = NULL;
]
    if (head == NULL)
    {
        head = newNode;
        return;
    }
    struct Node* temp = head;
    while (temp->next != NULL)
        temp = temp->next;
    temp->next = newNode;
    newNode->prev = temp;
}
void delete()
 {
    if (head == NULL)
    {
        printf("List is empty\n");
        return;
    }
    struct Node* temp = head;
    if (temp->next == NULL)
    {
        free(head);
        head = NULL;
        return;
    }
    while (temp->next != NULL)
        temp = temp->next;

    temp->prev->next = NULL;
    free(temp);
 }
void display()
{
    struct Node* temp = head;
    while (temp != NULL)
    {
        printf("%c ", temp->data);
        temp = temp->next;
    }
    printf("\n");
}
```

## Output:
![Screenshot 2025-05-07 184002](https://github.com/user-attachments/assets/cd0c9256-db31-4815-9dd8-e028a5169640)



## Result:
Thus the program was executed and the output was verified successfully.
