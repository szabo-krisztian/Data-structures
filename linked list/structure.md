# Data Structures - Linked list

Structure implementation:
```c
struct Node
{
    int data;
    struct Node* next;
};

struct Node* head; // global variable, first element in the chain
```

Traversing a linked list, and printing it's data:
```c
void Print()
{
    struct Node* temp = head;
    printf("List is: ");

    while (temp != NULL)
    {
        printf(" %d", temp->data);
        temp = temp->next;
    }
    printf("\n");
}
```

Inserting an element, with specified data value:
```c
void Insert(int x)
{
    struct Node* temp = (Node*)malloc(sizeof(Node));
    temp->data = x;
    temp->next = head;
    head = temp;
}
```

