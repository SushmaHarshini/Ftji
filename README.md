# Ftji
class Node:
    def __init__(self,data):
        self.data = data
        self.next = None
class linkedlist:
    def __init__(self):
        self.head = None

    def b_insert(self,data):
        newnode = Node(data)
        newnode.next = self.head
        self.head = newnode
    def display(self):
        if self.head is None:
            print("empty")
            return
        cur = self.head
        while cur:
            print(cur.data,end="->")
            cur = cur.next

obj = linkedlist()

obj.display()
