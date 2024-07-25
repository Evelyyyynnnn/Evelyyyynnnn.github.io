---
title: CS Exercise-3.Binary Search
tags: Interview
date: 2023-09-11 10:15:38
---

# Binary Search

##   1.Easy

### (35) Search Insert Position


#### Method 1：Biscant
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


#### Method 2: Traditional Index

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


##   2.Medium

###   (33)Search in Rotated Sorted Array

###   (34)Find First and Last Position of Element in Sorted Array

###   (240)Search a 2D Matrix II

###   (300)Longest Increasing Subsequence

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


