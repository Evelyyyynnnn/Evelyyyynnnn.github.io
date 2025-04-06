---
title: CS Exercise-The Simplest Greedy Algo
tags: Interview
date: 2025-04-11 10:15:38
---

# Greedy

##   2.Medium

###   (55)Jump Game

###   (253)Meeting Rooms II

###   (406)Queue Reconstruction by Height

###   (581)Shortest Unsorted Continuous Subarray

###   (621)Task Scheduler

### (680) Valid Palindrome II

<a name="680"></a>

```python
class Solution(object):
    def validPalindrome(self, s):
        l,r=0,len(s)-1
        while l<r:
            if s[l]!=s[r]:
                return s[l+1:r+1] == s[l+1:r+1][::-1] or s[l:r] == s[l:r][::-1]
            l+=1
            r-=1
        return True
```

            

Palindrome questions:
[(9) Palindrome Number](/2023/09/11/Interview/CS-Tutorial/1.The-Simplest-Greedy-Algo/Math/index.html#9)
[(345) Reverse Vowels of a String](/2023/09/11/Interview/CS-Tutorial/1.The-Simplest-Greedy-Algo/Math/index.html#345)
[(680) Valid Palindrome II](/2023/09/11/Interview/CS-Tutorial/2.Mastering-Two-Pointers/Two-Pointers/index.html#680)