## Name: Naneshvaran C
## Reg.no:212224110038
EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.
Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:
```
#include <stdio.h>
#define MAX 100

int main() {
    int stack[MAX], top = -1, n, i, choice;

    while(1) {
        printf("\n1. Push\n2. Pop\n3. Display Stack\n4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch(choice) {
            case 1:
                if(top == MAX - 1) {
                    printf("Stack Overflow!\n");
                } else {
                    int element;
                    printf("Enter element to push: ");
                    scanf("%d", &element);
                    stack[++top] = element;
                }
                break;

            case 2:
                if(top == -1) {
                    printf("Stack Underflow!\n");
                } else {
                    printf("Popped element: %d\n", stack[top--]);
                }
                break;

            case 3:
                if(top == -1) {
                    printf("Stack is empty.\n");
                } else {
                    printf("Stack elements: ");
                    for(i = 0; i <= top; i++) {
                        printf("%d ", stack[i]);
                    }
                    printf("\n");
                }
                break;

            case 4:
                return 0;

            default:
                printf("Invalid choice! Try again.\n");
        }
    }

    return 0;
}
```
Output:

<img width="1228" height="627" alt="image" src="https://github.com/user-attachments/assets/51cdd828-7913-4206-9edd-dc493fab9618" />


Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:
```
#include <stdio.h>
#define MAX 100

int main() {
    int stack[MAX], top = -1;
    int element;

    printf("Enter element to push into the stack: ");
    scanf("%d", &element);

    if(top == MAX - 1) {
        printf("Stack Overflow! Cannot push element.\n");
    } else {
        stack[++top] = element;
        printf("Element %d pushed into the stack.\n", element);
    }

    // Display stack elements
    printf("Stack elements: ");
    for(int i = 0; i <= top; i++) {
        printf("%d ", stack[i]);
    }
    printf("\n");

    return 0;
}
```
Output:

<img width="1447" height="710" alt="image" src="https://github.com/user-attachments/assets/7b6f246e-b311-4871-b1ab-cb77aa09858c" />


Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
#include <stdio.h>
#define MAX 100

int main() {
    int queue[MAX], front = -1, rear = -1;
    int choice, element, i;

    while(1) {
        printf("\n1. Enqueue\n2. Dequeue\n3. Display Queue\n4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch(choice) {
            case 1: // Enqueue
                if(rear == MAX - 1) {
                    printf("Queue Overflow!\n");
                } else {
                    printf("Enter element to enqueue: ");
                    scanf("%d", &element);
                    if(front == -1) front = 0; // First element
                    queue[++rear] = element;
                }
                break;

            case 2: // Dequeue
                if(front == -1 || front > rear) {
                    printf("Queue Underflow!\n");
                    front = -1;
                    rear = -1;
                } else {
                    printf("Dequeued element: %d\n", queue[front++]);
                }
                break;

            case 3: // Display
                if(front == -1 || front > rear) {
                    printf("Queue is empty.\n");
                } else {
                    printf("Queue elements: ");
                    for(i = front; i <= rear; i++) {
                        printf("%d ", queue[i]);
                    }
                    printf("\n");
                }
                break;

            case 4:
                return 0;

            default:
                printf("Invalid choice! Try again.\n");
        }
    }

    return 0;
}
```
Output:

<img width="1474" height="679" alt="image" src="https://github.com/user-attachments/assets/03402e21-c35a-4f15-9c05-81746bdb9eb8" />

Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:
```
#include <stdio.h>
#define MAX 100

int main() {
    int queue[MAX], front = -1, rear = -1;
    int n, element, i;

    printf("Enter number of elements to insert into the queue: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        if(rear == MAX - 1) {
            printf("Queue Overflow! Cannot insert more elements.\n");
            break;
        }
        printf("Enter element %d: ", i + 1);
        scanf("%d", &element);
        if(front == -1) front = 0;  // First element
        queue[++rear] = element;
    }

    // Display queue elements
    if(front == -1) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements: ");
        for(i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }

    return 0;
}
```
Output:
<img width="1506" height="623" alt="image" src="https://github.com/user-attachments/assets/902cd659-4282-450a-9a8c-bc6d23478268" />


Result:
Thus, the program to insert elements in queue using array is verified successfully.

 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY
Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:
```
#include <stdio.h>
#define MAX 100

int front = -1, rear = -1;
int queue[MAX];

// Function to delete (dequeue) an element
void dequeue() {
    if(front == -1 || front > rear) {
        printf("Queue Underflow! No elements to delete.\n");
        front = -1;
        rear = -1;
    } else {
        printf("Deleted element: %d\n", queue[front++]);
    }
}

int main() {
    int n, i, element;

    printf("Enter number of elements to insert into the queue: ");
    scanf("%d", &n);

    for(i = 0; i < n; i++) {
        if(rear == MAX - 1) {
            printf("Queue Overflow! Cannot insert more elements.\n");
            break;
        }
        printf("Enter element %d: ", i + 1);
        scanf("%d", &element);
        if(front == -1) front = 0;
        queue[++rear] = element;
    }

    printf("\nQueue elements before deletion: ");
    for(i = front; i <= rear; i++) {
        printf("%d ", queue[i]);
    }
    printf("\n");

    // Delete elements
    dequeue();
    dequeue();

    printf("Queue elements after deletion: ");
    for(i = front; i <= rear; i++) {
        printf("%d ", queue[i]);
    }
    printf("\n");

    return 0;
}
```

Output:
<img width="1459" height="695" alt="image" src="https://github.com/user-attachments/assets/e622746a-a3d0-4bbc-9e73-0f250ee1c0d5" />

Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
