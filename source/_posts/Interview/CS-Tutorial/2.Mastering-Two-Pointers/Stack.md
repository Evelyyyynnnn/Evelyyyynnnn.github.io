---
title: CS Exercise
tags: Interview
date: 2023-09-11 10:15:38
---

# Stack

##   1.Easy


### (20) Valid Parentheses

Given a string s containing just the characters ${ }^1\left({ }^1,{ }^1\right)^1,{ }^1\left\{{ }^1,{ }^1\right\}^1,{ }^1\left[{ }^1 \text { and }{ }^1\right]^1$, determine if the input string is valid.
An input string is valid if:
1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.

强制性匹配规则下[{]}就是错误的


```python
class Solution:
    def isValid(self, s): 
        valid_brack = [('{', '}'), ('(', ')'), ('[', ']')]
        stack = []
        for c in s:
            if len(stack)>0 and (stack[-1], c) in valid_brack:
                stack.pop()
            else:
                stack.append(c)
        return len(stack)==0
```
###   (155)Min Stack

##   2.Medium

###   (94)Binary Tree Inorder Traversal

###   (114)Flatten Binary Tree to Linked List

###   (227)Basic Calculator II

###   (394)Decode String

###   (581)Shortest Unsorted Continuous Subarray

###   (739)Daily Temperatures

##   3.Hard

###   (32)Longest Valid Parentheses

###   (84)Largest Rectangle in Histogram

###   (85)Maximal Rectangle

