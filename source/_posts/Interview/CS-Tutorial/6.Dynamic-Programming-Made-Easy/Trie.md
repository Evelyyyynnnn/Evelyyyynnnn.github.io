---
title: CS Exercise
tags: Interview
date: 2023-09-11 10:15:38
---

# Trie
## (13) Roman to Integer
I can be placed before V (5) and X (10) to make 4 and 9. 
X can be placed before L (50) and C (100) to make 40 and 90. 
C can be placed before D (500) and M (1000) to make 400 and 900.

```python
class Solution:
    def romanToInt(self,s):
        translation={
            "I":1,
            "V":5,
            "X":10,
            "L":50,
            "C":100,
            "D":500,
            "M":1000
        }
        number=0
        s = s.replace("IV", "IIII").replace("IX", "VIIII")
        s = s.replace("XL", "XXXX").replace("XC", "LXXXX")
        s = s.replace("CD", "CCCC").replace("CM", "DCCCC")
        for char in s:
            number +=translation[char]
        return number
```


##   2.Medium

###   (139)Word Break

###   (208)Implement Trie (Prefix Tree)

