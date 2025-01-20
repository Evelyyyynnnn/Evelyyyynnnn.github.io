---
title: CS Exercise-Overview
tags: Interview
date: 2023-09-11 10:15:38
---

*<small>[Home](/About/index.html) > [Interview](/tags/Interview/index.html) > [CS Tutorial](/2023/09/11/Interview/CS-Tutorial/CS-Tutorial/index.html) > **[Interview Qs](/2023/09/11/Interview/CS-Tutorial/Interview-Qs/index.html) </small>***


### 1. Normal Function VS类函数

```python
def two_sum(nums, target):
    for i in range(len(nums)):
        for j in range(i+1, len(nums)):
            if nums[j] == target - nums[i]:
                return [i, j]

nums = [2, 7, 8, 9]
target = 9
result = two_sum(nums, target)
print(result)  


#类函数
class Solution:
    def two_sum(self, nums, target):
        for i in range(len(nums)):
            for j in range(i+1, len(nums)):
                if nums[j] == target - nums[i]:
                    return [i, j]

# 创建 Solution 类的实例
solution = Solution()

# 调用 two_sum 方法
nums = [2, 7, 8, 9]
target = 9
result = solution.two_sum(nums, target)
print(result) 
```

### 2.函数内部赋值


```python
##报错原因：在函数内部对nums的赋值仅在函数内部有效，并没有原地修改输入的nums数组
class Solution(object):
    def removeElement(self, nums, val):
        blanket=[]
        for i,ch in enumerate(nums):
            if nums[i] != val:
                blanket.append(ch)
        nums=blanket
        return len(blanket),nums

solution = Solution()
val=3
nums = [3,2,2,3]
result = solution.removeElement(nums,val)
print(result)

```

### Data Cleaning and Matrix Processing 


```python
# index place
positions.loc[spread.index[i], 'long'] = capital / prices1[i]
#cumulative multiply
cumulative_returns = x.cumprod()

```