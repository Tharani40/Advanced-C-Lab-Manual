EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

    struct Node{
        char data; 
        struct Node *next;
    }*head;
    
    void search(char data)
    {
        char item=data;
        int i=0,f=0;
        struct Node*temp;
        temp=head;
        if(temp==NULL){
            printf("Item not found");
        }
          else{
            while(temp!=NULL){
                if(temp->data==item){
                    printf("item %c found at location %d",item,i+1);
                
                f=1;
              }
              i++;
              temp=temp->next;      
          }        
      }
      if(f==0)
      {
                  printf("Item not found");
      }
    }
  
Output:

![444777037-6556110f-3d55-4307-84af-2fe5fe69b0b7](https://github.com/user-attachments/assets/1a6613bb-5073-4561-bf38-9672a1923c5a)


Result:

Thus, the program to search a given element in the given linked list is verified successfully.


 
EXP NO:17  PROGRAM TO INSERT A NODE IN A LINKED LIST.
Aim:
To write a C program to insert a node in a linked list.
Algorithm:
1.	Define the structure for a node in a linked list
2.	Define the insert function to insert a new node with character data at the end of the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the insert function and perform other linked list operations as needed.
 
Program:

    struct Node{
        char data; 
        struct Node *next;
    }*head;
    
    void insert(char data)
    {
        struct Node *newnode,*temp;
        newnode=(struct Node*)malloc(sizeof(struct Node));
        newnode->data=data;
        newnode->next=NULL;
        if(head==NULL){
            head=newnode;
        }
        else{
            temp=head;
            while(temp->next!=NULL){
                temp=temp->next;
            }
            temp->next=newnode;
        }
        
    }
Output:

 ![444777070-11f31c7e-35f0-477a-8ea6-79d141771aac](https://github.com/user-attachments/assets/b015dfbb-2076-42a0-bd7b-f1a2aaa17c4c)

Result:

Thus, the program to insert a node in a linked list is verified successfully.


 
EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST
Aim:
To write a C program to traverse a doubly linked list.

Algorithm:
1.	Initialize a temporary pointer (temp) to the head of the list.
2.	Use a while loop to traverse the list until the end (temp == NULL) is reached.
3.	Inside the loop, print the data of the current node.
4.	Move to the next node by updating the temp pointer to point to the next node (temp = temp->next).
 
Program:

    struct Node
    {
        struct Node *prev;
        struct Node *next;
        int data;
    }*head;
    
    void display()
    {
        struct Node*temp;
        temp=head;
        while(temp!=NULL){
            printf("%d\n",temp->data);
            temp=temp->next;
        }        
    }
Output:

![444777091-9591d2e4-afc4-48d6-9e71-4f219ca605a9](https://github.com/user-attachments/assets/a9311bfd-be17-40cc-a85c-8bbe77d37eb6)


Result:

Thus, the program to traverse a doubly linked list is verified successfully. 



EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST
Aim:
To write a C program to insert an element in doubly linked list

Algorithm:
1.	Create a new node (newNode) and allocate memory for it.
2.	Set the data of the new node to the provided value.
3.	If the list is empty, set the new node as the head.
4.	If the list is not empty, traverse the list to find the last node.
5.	Set the new node's prev pointer to the last node and update the last node's next pointer to the new node.
 
Program:

      struct Node
      {
          float data;
          struct Node *prev;
          struct Node *next;
      }*head;
      
      void insert(float data)
      {
          struct Node *temp,*newnode;
          newnode=(struct Node*)malloc(sizeof(struct Node));
          newnode->data=data;
          newnode->next=NULL;
          newnode->prev=NULL;
          if(head==NULL){
              head=newnode;
          }
          else{
              temp=head;
              while(temp->next!=NULL){
                  temp=temp->next;
              }
              temp->next=newnode;
              newnode->prev=temp;
          }        
      }
Output:

![444777122-0e6deed1-0706-4f8b-99fa-a5c563e1b61c](https://github.com/user-attachments/assets/4eb2ed88-a1c2-4d3c-8084-21c463fdf5d9)


Result:

Thus, the program to insert an element in doubly linked list is verified successfully.




EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST




Aim:
To write a C function that deletes a given element from a linked list.

Algorithm:
1.	Check if the Linked List is Empty:
o	If the head of the linked list is NULL, print a message indicating the list is empty and exit the function.
2.	Traverse the Linked List:
o	Start from the head node and iterate through the list to find the node that contains the given element (data).
3.	Handle Deletion of the First Node:
o	If the element to be deleted is found in the head node:
	Update the head of the linked list to point to the next node (i.e., head = head->next).
	Free the memory allocated to the node to be deleted.
	Exit the function.
4.	Traverse and Delete from the Middle or End:
o	If the element is not in the head node, continue traversing the list by checking each node’s next pointer.
o	When the node with the element is found, update the previous node’s next pointer to point to the next node of the node to be deleted (prev->next = current->next).
o	Free the memory allocated to the node to be deleted.
5.	Handle the Case when the Element is Not Found:
o	If the element is not found in any node, print a message indicating the element is not present in the list.
6.	End the Function.


Program:
     struct Node
     {
         int data; 
         struct Node *next;
     }*head;
     void delete()
     {
         struct Node *ptr;
         if(head == NULL)
         {
             printf("List is empty\n");
         }
         else
         {
             ptr = head;
             head = ptr->next;
             free(ptr);
             printf("Node deleted from the begining ...\n");
         }
     }

Output:


![444777152-9d601cbb-a243-48e3-8ae4-7f0e4519baf4](https://github.com/user-attachments/assets/7e2d23e9-5dea-46dc-a283-3097a115b0d7)





Result:

Thus, the function that deletes a given element from a linked list is verified successfully.
