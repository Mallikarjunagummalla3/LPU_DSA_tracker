# find middle node(show-fast pointer)
link https://leetcode.com/problems/middle-of-the-linked-list/solutions/287950/fast-and-slow-pointer/

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

def find_middle(head):
    slow = head
    fast = head

    while fast and fast.next:
        slow = slow.next          # Move 1 step
        fast = fast.next.next     # Move 2 steps

    return slow

head = Node(1)
head.next = Node(2)
head.next.next = Node(3)
head.next.next.next = Node(4)
head.next.next.next.next = Node(5)

middle = find_middle(head)
print("Middle Node:", middle.data)
```