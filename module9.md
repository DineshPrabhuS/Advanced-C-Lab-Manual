***EXP NO:11*** C FUNCTION TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C function to display stack elements using an array.

Algorithm:
1. Declare a character array stack[100] and an integer variable top initialized to -1.
2. Define a function display().
3. If top is equal to -1:
    a. Print "stack is empty".
4. Else:
    a. Loop from i = top down to 0:
        i. Print stack[i] followed by a newline.
5. End function.

Program:
```
char stack[100];
int top = -1;
void display()
{
    if(top == -1){
        printf("stack is empty\n");
    }
    else{
        for(int i = top; i >= 0; i--){
        printf("%c\n",stack[i]);
        }
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/dff9bc6c-a871-4fcb-8616-f2eb34473f54)


Result:
Thus, the program to display stack elements using an array is verified successfully.
 

***EXP NO:12*** C FUNCTION TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.

Aim:
To create a C function to push the given element in to a stack using array.

Algorithm:
1. Declare a character array stack[100].
2. Declare integer variables size = 3 and top = -1.
3. Define the function push with parameter data (character).
4. If top < size - 1:
    a. Increment top by 1.
    b. Assign data to stack[top].
5. Else:
    a. Print "stack is full".
6. End function.

 
Program:

```
char stack[100];
int size=3,top=-1;
void push (char data)
{
    if(top < size - 1){
        top = top + 1;
        stack[top] = data;
    }
    else{
        printf("stack is full\n");
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/892e5d53-95cc-407c-8fb8-a7f8e4c1c0c9)


Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
***EXP NO:13*** C FUNCTION TO DISPLAY QUEUE ELEMENTS USING ARRAY.

Aim:
To write a C function to display queue elements using array

Algorithm:
1. Declare a float array queue[50].
2. Declare integer variables rear and front.
3. Define the function display().
4. If front == -1 or front > rear:
    a. Print "No elements to display".
5. Else:
    a. Loop from i = front to i <= rear:
        i. Print queue[i] with one decimal place.
6. End function.

 
Program:

```
float queue[50];
int rear, front;
void display()
{
    if(front == -1 || front > rear){
        printf("No elements to display\n");
    }
    else{
        for(int i = front; i <= rear; i++){
        printf("%.1f\n", queue[i]);
        }
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/43e93b91-a74a-464a-a01b-bf1da58e563a)


Result:
Thus, the program to display queue elements using array is verified successfully.


 
***EXP NO:14*** C FUNCTION TO INSERT ELEMENTS IN QUEUE USING ARRAY.

Aim:
To write a C function to insert elements in queue using array.

Algorithm:
1. Declare integer variables size = 10, front, and rear.
2. Declare a float array queue[50].
3. Define the function enqueue() with a float parameter data.
4. If rear < size:
    a. If front == -1, set front = 0.
    b. Increment rear by 1.
    c. Assign data to queue[rear].
5. End function.

Program:

```
int size = 10, rear, front;
float queue[50];
void enqueue(float data)
{
    if(rear < size){
        if(front == -1) front = 0;
        rear++;
        queue[rear] = data;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/63f3d9b3-c420-4fe4-80a1-3a72c6c2f464)


Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
***EXP NO:15*** C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY

Aim:
To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:
1. Declare integer variables front and rear.
2. Define the function dequeue().
3. If front == -1 or front > rear:
    a. Print "Queue underflow".
4. Else:
    a. Increment front by 1.
5. End function.


Program:

```
int front, rear;
void dequeue()
{
    if(front == -1 || front > rear){
        printf("Queue underflow\n");
    }
    else{
        front = front + 1;
    }
}
```

Output:

![image](https://github.com/user-attachments/assets/40071c99-282e-4a4d-8337-f585f8f29161)


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
