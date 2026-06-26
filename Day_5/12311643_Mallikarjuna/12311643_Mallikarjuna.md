# find middle node(show-fast pointer)
link https://leetcode.com/problems/middle-of-the-linked-list/solutions/287950/fast-and-slow-pointer/

```python
class Solution(object):
    def middleNode(self, head):
        slow = head
        fast = head

        while fast is not None and fast.next is not None:
            slow = slow.next
            fast = fast.next.next

        return slow
```


