---
title: CS Exercise
tags: Interview
date: 2023-09-11 10:15:38
---

# Binary Search

## (35) Search Insert Position

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