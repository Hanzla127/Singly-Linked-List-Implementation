
# Singly-Linked-List-Implementation
Custom Linked List Implementation – Implements a singly linked list with various operations.
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        last = self.head
        while last.next:
            last = last.next
        last.next = new_node

    def display(self):
        current = self.head
        while current:
            print(current.data, end=" -> ")
            current = current.next
        print("None")
        if __name__ == "__main__":
    ll = LinkedList()
    ll.append(1)
    ll.append(2)
    ll.append(3)
    ll.display()
