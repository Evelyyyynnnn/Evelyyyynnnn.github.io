---
title: CS Exercise
tags: Interview
date: 2023-09-11 10:15:38
---

# Linked List

##   1.Easy



## (21)Merge Two Sorted Lists

```python
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

###   (141)Linked List Cycle

###   (206)Reverse Linked List

##   2.Medium

###   (5)Longest Palindromic Substring

###   (19)Remove Nth Node From End of List

###   (114)Flatten Binary Tree to Linked List

###   (142)Linked List Cycle II

###   (146)LRU Cache

###   (148)Sort List

##   3.Hard

###   (23)Merge k Sorted Lists
