---
title: CS Exercise-The Simplest Greedy Algo
tags: Interview
date: 2023-09-11 10:15:38
---

# Array

##   1.Easy


### (1). Two Sum

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

###   (2)Add Two Numbers
###   (4)Median of Two Sorted Arrays


### (26) Remove Element from Sorted Array
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

## (27) Remove Elements

```python
class Solution(object):
    def removeElement(self, nums, val):
        index=0
        for i in range(len(nums)):
            if nums[i]!=val:
                nums[index]=nums[i]
                index+=1
        return index

solution = Solution()
val=3
nums = [3,2,2,3]
result = solution.removeElement(nums,val)
print(result)
```

## (35) Search Insert Position

### Method 1：Biscant
```python
class Solution(object):
    def searchInsert(self, nums, target):
        left=0
        right=len(nums)-1
        
        while left<=right:
            mid=(left+right)//2
            if nums[mid]==target:
                return mid
            elif nums[mid]>target:
                right=mid-1
            else:
                left=mid+1
        return left
```
<!-- #报错原因
- `for i in range(len(nums))`：这个循环会从索引`0`开始迭代到数组的最后一个索引。
- 在第一次循环迭代时，“if nums[i] == target”检查是否找到了`target`，如果找到了，返回索引。
- `elif nums[i] < target and nums[i+1] > target` : 这个条件检查是否” target”应该插入到 `nums[i]`和` nums $[i+1$ ]`之间。
- `else”：如果以上条件都不满足，就返回`len(nums)” -->

### Method 2: Traditional Index

```python
class Solution(object):
    def searchInsert(self, nums, target):
        k=0
        s=0
        for i in range(len(nums)):
            if nums[i]!=target:
                k+=1
            else:
                return k
        for j in range(1,len(nums)):
            if nums[j-1] < target:
                if nums[j] > target:
                    return j
        return(len(nums))
```

## (66) Plus One

<!-- 格式转换版(一) -->
```python
class Solution:
    def plusOne(self, digits) :
        digits = int(''.join(map(str, digits)))
        digits+=1
        digits = [int(digit) for digit in str(digits)]
        return digits
```

<!-- 格式转换版(二) -->
```python
class Solution:
    def plusOne(self, digits):
        idx=len(digits)-1
        while idx>=0:
            if digits[idx]==9:
                digits[idx]=0
            else:
                digits[idx]+=1
                return digits
            idx -=1
        return digits
```

<!-- index方法一 -->
```python
class Solution:
    def plusOne(self, digits): 
        for i, d in reversed(list(enumerate(digits))):
            if d < 9:
                digits[i] += 1
            return digits
            digits[i] = 0

        return [1] + digits
```

###   (121)Best Time to Buy and Sell Stock

###   (136)Single Number

###   (169)Majority Element

###   (283)Move Zeroes

###   (448)Find All Numbers Disappeared in an Array

##   2.Medium

###   (15)3Sum

###   (31)Next Permutation

###   (33)Search in Rotated Sorted Array

###   (34)Find First and Last Position of Element in Sorted Array

###   (53)Maximum Subarray

###   (55)Jump Game

###   (56)Merge Intervals

###   (64)Minimum Path Sum

###   (79)Word Search

###   (105)Construct Binary Tree from Preorder and Inorder Traversal

###   (128)Longest Consecutive Sequence

###   (139)Word Break

###   (152)Maximum Product Subarray

###   (198)House Robber

###   (200)Number of Islands

###   (215)Kth Largest Element in an Array

###   (221)Maximal Square

###   (238)Product of Array Except Self

###   (240)Search a 2D Matrix II

###   (253)Meeting Rooms II

###   (300)Longest Increasing Subsequence

###   (309)Best Time to Buy and Sell Stock with Cooldown

###   (338)Counting Bits

###   (347)Top K Frequent Elements

###   (399)Evaluate Division

###   (406)Queue Reconstruction by Height

###   (416)Partition Equal Subset Sum

###   (581)Shortest Unsorted Continuous Subarray

###   (621)Task Scheduler

###   (739)Daily Temperatures

##   3.Hard

###   (84)Largest Rectangle in Histogram

###   (85)Maximal Rectangle

###   (239)Sliding Window Maximum

###   (312)Burst Balloons

