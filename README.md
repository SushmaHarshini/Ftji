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

    def e_insert(self,data):
        newnode = Node(data)
        if self.head is None:
            self.head = newnode
            return
        cur = self.head
        while cur.next:
          cur = cur.next
        cur.next = newnode


    def b_delete(self):
        if self.head is None:
            print("empty")
            return
        self.head  = self.head.next

    def e_delete(self):
        if self.head is None:
            print("empty")
            return
        if self.head.next is None:
            self.head = None
            return
        cur = self.head
        while cur.next.next:
            cur = cur.next
        cur.next =None


obj = linkedlist()


obj.display()
print()
obj.e_delete()
