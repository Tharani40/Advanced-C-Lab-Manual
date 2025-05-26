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

      #include <stdio.h>
      #define SIZE 5
      
      int stack[SIZE], top = -1;
      
      void push(int value) {
          if (top == SIZE - 1)
              printf("Stack Overflow\n");
          else
              stack[++top] = value;
      }
      
      void display() {
          if (top == -1)
              printf("Stack is empty\n");
          else {
              printf("Stack elements:\n");
              for (int i = top; i >= 0; i--)
                  printf("%d\n", stack[i]);
          }
      }
      
      int main() {
          push(10);
          push(20);
          push(30);
          display();
          return 0;
      }


Output:

![444776608-82e2790f-8bf1-4996-b528-521b1372f9f6](https://github.com/user-attachments/assets/6559d111-afe9-4dde-9b62-c0ce981673c1)





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



     #include <stdio.h>
     #define SIZE 5
     
     int stack[SIZE], top = -1;
     
     void push(int value) {
         if (top == SIZE - 1)
             printf("Stack Overflow\n");
         else {
             stack[++top] = value;
             printf("%d pushed into stack\n", value);
         }
     }
     
     int main() {
         push(5);
         push(10);
         push(15);
         return 0;
     }

Output:

![444776646-59f4bfad-fefb-45d4-af53-215b43140848](https://github.com/user-attachments/assets/cd751e3c-2ae6-40e9-a13b-b1b283f56726)


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

      #include <stdio.h>
      #define SIZE 5
      
      int queue[SIZE], front = -1, rear = -1;
      
      void enqueue(int value) {
          if (rear == SIZE - 1)
              printf("Queue Overflow\n");
          else {
              if (front == -1) front = 0;
              queue[++rear] = value;
          }
      }
      
      void display() {
          if (front == -1 || front > rear)
              printf("Queue is empty\n");
          else {
              printf("Queue elements:\n");
              for (int i = front; i <= rear; i++)
                  printf("%d\n", queue[i]);
          }
      }
      
      int main() {
          enqueue(10);
          enqueue(20);
          enqueue(30);
          display();
          return 0;
      }

Output:



![444776680-9dd29872-05c2-4ace-8a3d-27fef0631db5](https://github.com/user-attachments/assets/2f954bcf-279f-4527-b7ca-fa6c297f7d1b)

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

     #include <stdio.h>
     #define SIZE 5
     
     int queue[SIZE], front = -1, rear = -1;
     
     void enqueue(int value) {
         if (rear == SIZE - 1)
             printf("Queue Overflow\n");
         else {
             if (front == -1) front = 0;
             queue[++rear] = value;
             printf("%d inserted into queue\n", value);
         }
     }
     
     int main() {
         enqueue(5);
         enqueue(10);
         enqueue(15);
         return 0;
     }

Output:

![444776720-0c39c6aa-2d0a-4bb0-95b5-dbc7bf791e3f](https://github.com/user-attachments/assets/04a930f2-c8c7-4ace-b6f5-1eb7be34c1f1)


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

      #include <stdio.h>
      #define SIZE 5
      
      int queue[SIZE], front = -1, rear = -1;
      
      void enqueue(int value) {
          if (rear == SIZE - 1)
              printf("Queue Overflow\n");
          else {
              if (front == -1) front = 0;
              queue[++rear] = value;
          }
      }
      
      void dequeue() {
          if (front == -1 || front > rear)
              printf("Queue Underflow\n");
          else
              printf("%d deleted from queue\n", queue[front++]);
      }
      
      int main() {
          enqueue(10);
          enqueue(20);
          enqueue(30);
          dequeue();
          dequeue();
          return 0;
      }

Output:


![444776778-066b1118-06d0-4b81-83c9-6803ede21a86](https://github.com/user-attachments/assets/4f726c7f-dfdf-4595-92bc-6450e61422c4)


Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
