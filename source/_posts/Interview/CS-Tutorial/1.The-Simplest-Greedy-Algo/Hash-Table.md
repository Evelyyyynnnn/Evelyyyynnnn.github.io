---
title: CS Exercise
tags: Interview
date: 2023-09-11 10:15:38
---

# Hash Table


## (1) Two Sum

Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice.假设一组矩阵中只有一组数对作为最终结果

You can return the answer in any order.

```python
class Solution:
    def two_sum(self, nums, target):
        for i in range(len(nums)):
            for j in range(i+1, len(nums)):
                if nums[j] == target - nums[i]:
                    return [i, j]
```


## (1) Two Sum

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

##   1.Easy

###   (2)Add Two Numbers

###   (4)Median of Two Sorted Arrays

###   (141)Linked List Cycle

###   (169)Majority Element

###   (448)Find All Numbers Disappeared in an Array

##   2.Medium

###   (105)Construct Binary Tree from Preorder and Inorder Traversal

###   (128)Longest Consecutive Sequence

###   (139)Word Break

###   (142)Linked List Cycle II

###   (146)LRU Cache

###   (208)Implement Trie (Prefix Tree)

###   (253)Meeting Rooms II

###   (347)Top K Frequent Elements

###   (438)Find All Anagrams in a String

###   (621)Task Scheduler

