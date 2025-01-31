---
title: CS Exercise-Overview
tags: Interview
date: 2023-09-11 10:15:38
---

*<small>[Home](/About/index.html) > [Interview](/tags/Interview/index.html) > [CS Tutorial](/2023/09/11/Interview/CS-Tutorial/CS-Tutorial/index.html) > **[Interview Qs](/2023/09/11/Interview/CS-Tutorial/Interview-Qs/index.html) </small>***

## Questions
### Question 1:
在一条单行道上，有n只乌龟向同一个方向爬行。他们的初始速度各不相同，可以假设分别为1(cm/s),2(cm/s).…n(cm/s),(假定vi小于vj,如果i小于j的话)且初始位置完全随机。由于是单行道，当后方的乌龟追上前方乌龟时，它将不得不减速，然后紧跟着前方乌龟爬行，形成一个小组。经过足够长的时间，乌龟们会分成多少组?

```python
#i:velocity;location[i]:position
location=[10,3,6,1,8]
location=[(i,location[i]) for i in range(len(location))]
location.sort(key=lambda x: x[1])
group=len(location)

for i in range(len(location)-1):
    j=i+1
    if location[i][0]>location[j][0]:
        group-=1
    i+=1

print(group,location,location[0],location[1])
```


## Knoeledge

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