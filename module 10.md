EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST.
Aim:
To write a C program to search a given element in the given linked list.

Algorithm:
1.	Define the structure for a node in a linked list.
2.	Define the search function to find a specific character in the linked list.
3.	Initialize the head of the linked list as needed.
4.	Call the search function and perform other linked list operations as needed.
 
Program:

```
struct Node{
    char data; 
    struct Node *next;
}*head;

void search(char data)
{
    int temp=data;
    struct Node *current=head;
    int count=1;
    int flag=0;
    while(current!=NULL)
    {
        if(current->data==temp)
        {
            printf("item %c found at location %d",current->data,count);
            flag=1;
        }
        count++;
        current=current->next;
    }
    if(flag==0)
    {
        printf("Item not found");
    }
}
```
Output:

![Screenshot 2025-04-27 052427](https://github.com/user-attachments/assets/be36b261-9b65-473f-a6d8-54755e09c843)


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

```
struct Node{
    int data; 
    struct Node *next;
}*head;
void insert(int data)
{
    struct Node *n=malloc(sizeof(struct Node));
    if(n==NULL)
    {
        printf("Memory allocation failed\n");
        return;
    }
    n->data=data;
    n->next=NULL;
    if(head==NULL)
        head=n;
    else
    {
        struct Node *temp=head;
        while(temp->next!=NULL)
        {
            temp=temp->next;
        }
        temp->next=n;
    }
}
```

Output:

![Screenshot 2025-04-27 052823](https://github.com/user-attachments/assets/3b472cc1-fe3e-4375-8dcd-e8a361190d81)


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

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    char data;
}*head;
void display()
{
    struct Node *current=head;
    while(current!=NULL)
    {
        printf("%c\n",current->data);
        current=current->next;
    }
}
```
Output:

![Screenshot 2025-04-27 054135](https://github.com/user-attachments/assets/1dbfbbdb-3908-4aeb-85bf-984932508221)


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

```
struct Node
{
    struct Node *prev;
    struct Node *next;
    float data;
}*head;
void insert(float data)
{
    struct Node *n=malloc(sizeof(struct Node));
    n->data=data;
    n->prev=NULL;
    n->next=NULL;
    if(head==NULL)
    {
        head=n;
    }
    else
    {
        struct Node *temp=head;
        while(temp->next!=NULL)
        {
            temp=temp->next;
        }
        temp->next=n;
        n->prev=NULL;
    }
    
}
```

Output:

![Screenshot 2025-04-27 054251](https://github.com/user-attachments/assets/43044083-1deb-452f-8c5d-6ff534b9d9cf)


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

```
struct Node{
    int data; 
    struct Node *next;
}*head;
void delete()
{
    struct Node *ptr=head;
    if(head==NULL)
    {
        printf("List is empty\n");
    }
    else
    {
        head=head->next;
        free(ptr);
        ptr=NULL;
        printf("Node deleted from the begining ...\n");
    }
}
```

Output:

![Screenshot 2025-04-27 054432](https://github.com/user-attachments/assets/dd411e01-81ff-4919-9646-98d6fc4138e4)






Result:
Thus, the function that deletes a given element from a linked list is verified successfully.





