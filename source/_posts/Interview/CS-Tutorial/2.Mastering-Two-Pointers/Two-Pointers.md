---
title: CS Exercise-The Simplest Greedy Algo
tags: Interview
date: 2023-09-11 10:15:38
---

# Two Pointers

##   1.Easy

###   (2)Add Two Numbers



## (26)Remove Element from Sorted Array
Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once.（巨大前提是数据广义单增） The relative order of the elements should be kept the same. Then return the number of unique elements in nums.

Consider the number of unique elements of nums to be k, to get accepted, you need to do the following things:

Change the array nums such that the first k elements of nums contain the unique elements in the order they were present in nums initially. The remaining elements of nums are not important as well as the size of nums. Return k.

```python
class Solution(object):
    def removeDuplicates(self, nums):
        dummy=1
        for i in range(1,len(nums)):
            if nums[i]!=nums[i-1]:
                nums[dummy]=nums[i]
                dummy+=1
        return dummy
```

## (27)Remove Elements
```python
class Solution(object):
    def removeElement(self, nums, val):
        index=0
        for i in range(len(nums)):
            if nums[i]!=val:
                nums[index]=nums[i]
                index+=1
        return index
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


###   (141)Linked List Cycle

###   (283)Move Zeroes


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

###   (5)Longest Palindromic Substring

###   (15)3Sum

###   (19)Remove Nth Node From End of List

###   (31)Next Permutation

###   (142)Linked List Cycle II

###   (148)Sort List

###   (253)Meeting Rooms II

###   (581)Shortest Unsorted Continuous Subarray

### (633)Sum of Square Numbers

```python
class Solution(object):
    def judgeSquareSum(self, c):
        for i in range(c):
            for j in range(c):
                if i**2+j**2==c:
                    return True
        return False
```

