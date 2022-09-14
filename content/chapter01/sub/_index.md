---
title: "1.4 Sub Level"
---

Có thể hiển thị thông tin ở sub level

{{< tabs "uniqueid" >}}
{{< tab "Java" >}}
```java
// Java program to count number of nodes in a linked list

/* Linked list Node*/
class Node
{
	int data;
	Node next;
	Node(int d) { data = d; next = null; }
}

// Linked List class
class LinkedList
{
	Node head; // head of list

	/* Inserts a new Node at front of the list. */
	public void push(int new_data)
	{
		/* 1 & 2: Allocate the Node &
				Put in the data*/
		Node new_node = new Node(new_data);

		/* 3. Make next of new Node as head */
		new_node.next = head;

		/* 4. Move the head to point to new Node */
		head = new_node;
	}

	/* Returns count of nodes in linked list */
	public int getCount()
	{
		Node temp = head;
		int count = 0;
		while (temp != null)
		{
			count++;
			temp = temp.next;
		}
		return count;
	}

	/* Driver program to test above functions. Ideally
	this function should be in a separate user class.
	It is kept here to keep code compact */
	public static void main(String[] args)
	{
		/* Start with the empty list */
		LinkedList llist = new LinkedList();
		llist.push(1);
		llist.push(3);
		llist.push(1);
		llist.push(2);
		llist.push(1);

		System.out.println("Count of nodes is " +
						llist.getCount());
	}
}
```
{{< /tab >}}
{{< tab "Python" >}}
```python
# A complete working Python program to find length of a
# Linked List iteratively
  
# Node class
class Node:
    # Function to initialise the node object
    def __init__(self, data):
        self.data = data # Assign data
        self.next = None # Initialize next as null
  
  
# Linked List class contains a Node object
class LinkedList:
  
    # Function to initialize head
    def __init__(self):
        self.head = None
  
  
    # This function is in LinkedList class. It inserts
    # a new node at the beginning of Linked List.
    def push(self, new_data):
  
        # 1 & 2: Allocate the Node &
        #     Put in the data
        new_node = Node(new_data)
  
        # 3. Make next of new Node as head
        new_node.next = self.head
  
        # 4. Move the head to point to new Node
        self.head = new_node
  
  
    # This function counts number of nodes in Linked List
    # iteratively, given 'node' as starting node.
    def getCount(self):
        temp = self.head # Initialise temp
        count = 0 # Initialise count
  
        # Loop while end of linked list is not reached
        while (temp):
            count += 1
            temp = temp.next
        return count
  
  
# Code execution starts here
if __name__=='__main__':
    llist = LinkedList()
    llist.push(1)
    llist.push(3)
    llist.push(1)
    llist.push(2)
    llist.push(1)
    print ("Count of nodes is :",llist.getCount())
```
{{< /tab >}}
{{< tab "C++" >}} # Windows Content {{< /tab >}}
{{< /tabs >}}