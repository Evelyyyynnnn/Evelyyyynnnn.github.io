---
title: CS Exercise
tags: Interview
date: 2023-09-11 10:15:38
---

# String

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

## (14)Longest Common Prefix最长公共前缀

```python
class Solution(object):
     def longestCommonPrefix(self, strs):

            if not strs:
                return ""
            shortest = min(strs,key=len)
            for i, ch in enumerate(shortest):
                for other in strs:
                    if other[i] != ch:
                        return shortest[:i]
            return shortest
```

## (20) Valid Parentheses
Given a string s containing just the characters ${ }^1\left({ }^1,{ }^1\right)^1,{ }^1\left\{{ }^1,{ }^1\right\}^1,{ }^1\left[{ }^1 \text { and }{ }^1\right]^1$, determine if the input string is valid.
An input string is valid if:
1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.

强制性匹配规则下"[{]}"就是错误的

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
    
solution = Solution()
s=")()"
result = solution.isValid(s)
print(result)  
```


## (28) Find the Index of the First Occurrence in a String

```python
class Solution(object):
    def strStr(self, haystack, needle):
        for i in range(len(haystack)):
            if haystack[i:i+len(needle)]==needle:
                return i
        return -1
```

## (58) Length of Last Word

```python
# 倒序
def lengthofLastWords(s):
    length=0
    i=len(s)-1
    while i>=0 and s[i]=='':
        i-=1
    while i>=0 and s[i]!='':
        length+=1
        i-=1
    return length

```

##   2.Medium

###   (10)Regular Expression Matching

###   (11)Container With Most Water

###   (17)Letter Combinations of a Phone Number

###   (139)Word Break

###   (208)Implement Trie (Prefix Tree)

###   (227)Basic Calculator II

###   (394)Decode String

###   (438)Find All Anagrams in a String

###   (647)Palindromic Substrings

##   3.Hard

###   (3)Longest Substring Without Repeating Characters

###   (32)Longest Valid Parentheses

###   (72)Edit Distance

###   (297)Serialize and Deserialize Binary Tree

###   (301)Remove Invalid Parentheses
