---
title: CS Exercise-The Simplest Greedy Algo
tags: Interview
date: 2023-09-11 10:15:38
---

# String

## General Knowledge

```python
# meaning for list
s=[1,2,3,4]
c='abcd'
print(s[1:4])
print(s[1:3])
print(s[0:3])
print(s[0])
print(s[3])
print(c[1:4])
print(c[1:3])
print(c[0:3])
print(c[0])
print(c[3])

[2, 3, 4]
[2, 3]
[1, 2, 3]
1
4
bcd
bc
abc
a
d
```

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

An input string is valid if:
1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.


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
###   (345)Reverse Vowels of a String
<a name="345"></a>

#### 知识点：
```python
s= "asvisl"
s_list=list(s)
c_list=list(reversed(s_list))
s=''.join(c_list)
print(s_list,c_list,s)

#result:['a', 's', 'v', 'i', 's', 'l'] ['l', 's', 'i', 'v', 's', 'a'] lsivsa

class Solution:
    def reverseVowels(self,s):
        s_list=list(s)
        c_list=list(reversed(s_list))
        s=''.join(c_list)
        return s
```
#### 答案：
```python
class Solution:
    def reverseVowels(self, s):
        Vowels=set('aeiouAEIOU')
        s=list(s)
        i,j=0,len(s)-1
        while i<j:
            if s[i] not in Vowels:
                i=i+1
            elif s[j] not in Vowels:
                j=j-1
            else: 
                s[i],s[j]=s[j],s[i]
                i=i+1
                j=j-1
        return ''.join(s)
```
Palindrome questions:
[(9) Palindrome Number](/2023/09/11/Interview/CS-Tutorial/1.The-Simplest-Greedy-Algo/Math/index.html#9)
[(345) Reverse Vowels of a String](/2023/09/11/Interview/CS-Tutorial/1.The-Simplest-Greedy-Algo/Math/index.html#345)
[(680) Valid Palindrome II](/2023/09/11/Interview/CS-Tutorial/2.Mastering-Two-Pointers/Two-Pointers/index.html#680)




###   (680)Valid Palindrome II
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
