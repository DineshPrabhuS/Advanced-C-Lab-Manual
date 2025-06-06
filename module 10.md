EXP NO:16 C FUNCTION TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.

Aim:
To write a C function to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
1. Define a structure Node with:
    a. A character data field.
    b. A pointer to the next Node.
2. Declare a global pointer head to the first node.
3. Define the function search() with a character parameter data.
4. Initialize a temporary pointer temp to head.
5. Initialize integer variables flag = 0 and i = 1.
6. While temp is not NULL:
    a. If temp->data is equal to data:
        i. Set flag = 1.
        ii. Break the loop.
    b. Increment i by 1.
    c. Move temp to temp->next.
7. If flag == 1:
    a. Print "item <data> found at location <i>".
8. Else:
    a. Print "Item not found".
9. End function.

Program:

```
struct Node{
    char data; 
    struct Node *next;
}*head;

void search(char data){
    struct Node *temp = head;
    int flag = 0, i = 1;
    while(temp != NULL){
        if(temp->data == data){
            flag = 1;
            break;
        }
        i++;
        temp = temp->next;
    }
    flag ? printf("item %c found at location %d", data, i) : printf("Item not found");
}
```

Output:

![image](https://github.com/user-attachments/assets/70a82a1a-78e2-4309-a33d-d7efa207e0fe)


Result:
Thus, the function to search a given element in the given linked list is verified successfully.


 
EXP NO:17 C FUNCTION TO INSERT A NODE IN A LINKED LIST.

Aim:
To write a C function to insert a node in a linked list.

Algorithm:
1. Define a structure Node with:
    a. An integer data field.
    b. A pointer to the next Node.
2. Declare a global pointer head to the first node.
3. Define the function insert() with an integer parameter data.
4. Create a new node n using dynamic memory allocation.
5. Assign data to n->data.
6. If head is NULL:
    a. Set head = n.
    b. Return from the function.
7. Else:
    a. Initialize a temporary pointer temp to head.
    b. Traverse the list until temp->next is NULL.
    c. Set temp->next = n.
8. End function.

 
Program:

```
struct Node{
    int data; 
    struct Node *next;
}*head;


void insert(int data)
{
    struct Node *n = (struct Node *) malloc (sizeof(struct Node));
    n -> data = data;
    if(head == NULL){
        head = n;
        return;
    }
    struct Node *temp = head;
    while(temp -> next != NULL){
        temp = temp -> next;
    }
    temp -> next = n;
}
```

Output:

![image](https://github.com/user-attachments/assets/07c569f5-2b42-4529-9243-772763dad51e)


 
Result:
Thus, the function to insert a node in a linked list is verified successfully.


 
EXP NO:18 C FUNCTION TO TRAVERSE A DOUBLY LINKED LIST

Aim:
To write a C function to traverse a doubly linked list.

Algorithm:
1. Define a structure Node with:
    a. A pointer to previous node (prev).
    b. A pointer to next node (next).
    c. An integer data field.
2. Declare a global pointer head to the first node.
3. Define the function display().
4. Initialize a temporary pointer temp to head.
5. While temp is not NULL:
    a. Print temp->data.
    b. Move temp to temp->next.
6. End function.
 
Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    int data;
}*head;

void display()
{
    struct Node *temp = head;
    while(temp != NULL){
        printf("%d\n", temp->data);
        temp = temp->next;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/c7724889-bf2a-451e-a1c8-de37e7fddc40)



Result:
Thus, the function to traverse a doubly linked list is verified successfully. 



EXP NO:19 C FUNCTION TO INSERT AN ELEMENT IN DOUBLY LINKED LIST

Aim:
To write a C function to insert an element in doubly linked list

Algorithm:
1. Define a structure Node with:
    a. A pointer to previous node (prev).
    b. A pointer to next node (next).
    c. A float data field.
2. Declare a global pointer head to the first node.
3. Define the function insert() with a float parameter data.
4. Create a new node n using dynamic memory allocation.
5. Assign data to n->data.
6. Set n->next to NULL.
7. If head is NULL:
    a. Set head = n.
    b. Set head->prev to NULL.
    c. Return from the function.
8. Else:
    a. Initialize a temporary pointer temp to head.
    b. Traverse the list until temp->next is NULL.
    c. Set temp->next = n.
    d. Set n->prev = temp.
9. End function.

Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void insert(float data)
{
    struct Node *n = (struct Node *) malloc (sizeof(struct Node));
    n -> data = data;
    n -> next = NULL;
    if(head == NULL){
        head = n;
        head -> prev = NULL;
        return;
    }
    struct Node *temp = head;
    while(temp -> next != NULL){
        temp = temp -> next;
    }
    temp -> next = n;
    n -> prev = temp;
}
```
Output:

![image](https://github.com/user-attachments/assets/37b7d583-6168-4e68-b348-80f2e87f073d)


Result:
Thus, the function to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1. Define a structure Node with:
    a. A pointer to previous node (prev).
    b. A pointer to next node (next).
    c. A float data field.
2. Declare a global pointer head to the first node.
3. Define the function delete().
4. If head is NULL:
    a. Print "UNDERFLOW".
    b. Return from the function.
5. Else:
    a. Move head to head->next (delete the first node).
    b. If head is not NULL:
        i. Set head->prev to NULL.
6. Print "Node deleted".
7. End function.



Program:

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;

void delete()
{
    if(head == NULL){
        printf("UNDERFLOW\n");
        return;
    }
    head = head->next;
    if(head != NULL){
        head->prev = NULL; 
    }
    printf("Node deleted\n");
}
```

Output:

![image](https://github.com/user-attachments/assets/2a829b55-28fb-4999-a898-67e2b67d0e83)


Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





