---
title: CS Exercise-The Simplest Greedy Algo
tags: Interview
date: 2023-09-11 10:15:38
---

# Math

##   1.Easy


## (9) Palindrome Number

<a name="9"></a>

```python
class Solution():
    def isPalindrome(self, s):
        s=str(s)
        return s==s[::-1]
```
Palindrome questions:
[(9) Palindrome Number](/2023/09/11/Interview/CS-Tutorial/1.The-Simplest-Greedy-Algo/Math/index.html#9)
[(345) Reverse Vowels of a String](/2023/09/11/Interview/CS-Tutorial/1.The-Simplest-Greedy-Algo/Math/index.html#345)
[(680) Valid Palindrome II](/2023/09/11/Interview/CS-Tutorial/2.Mastering-Two-Pointers/Two-Pointers/index.html#680)


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

## (66) Plus One

### 格式转换版(一)
```python
class Solution:
    def plusOne(self, digits) :
        digits = int(''.join(map(str, digits)))
        digits+=1
        digits = [int(digit) for digit in str(digits)]
        return digits
```
### 格式转换版(二)
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
### index方法二

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

###   (70)Climbing Stairs


##   2.Medium

###   (62)Unique Paths

###   (227)Basic Calculator II

###   (279)Perfect Squares

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

