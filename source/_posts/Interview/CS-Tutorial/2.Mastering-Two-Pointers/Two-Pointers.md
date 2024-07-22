---
title: CS Exercise
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

##   2.Medium

###   (5)Longest Palindromic Substring

###   (15)3Sum

###   (19)Remove Nth Node From End of List

###   (31)Next Permutation

###   (142)Linked List Cycle II

###   (148)Sort List

###   (253)Meeting Rooms II

###   (581)Shortest Unsorted Continuous Subarray

