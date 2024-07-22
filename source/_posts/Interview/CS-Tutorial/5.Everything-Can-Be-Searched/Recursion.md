---
title: CS Exercise
tags: Interview
date: 2023-09-11 10:15:38
---

# Recursion
##   1.Easy



### (21) Merge Two Sorted Lists

```python
# Definition for singly-linked list.
class ListNode(object):
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

class Solution(object):
    def mergeTwoLists(self, l1, l2):
        dummy = cur = ListNode(1)
        while l1 and l2:
            if l1.val < l2.val:
                cur.next = l1
                l1 = l1.next
            else:
                cur.next = l2
                l2 = l2.next
            cur = cur.next
        cur.next = l1 or l2
        return dummy.next
```

###   (206)Reverse Linked List

##   2.Medium

###   (394)Decode String

