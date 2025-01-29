

## Notebooks
xxxxx

## Exercise:

### 1. Group Anagrams

Given an array of strings `strs`, group all anagrams together into sublists. You may return the output in **any order**.

An **anagram** is a string that contains the exact same characters as another string, but the order of the characters can be different.

**Input**:  
`strs = ["act","pots","tops","cat","stop","hat"]`  
**Output**:  
`[["hat"],["act","cat"],["stop","pots","tops"]]`

**Input**:  
`strs = ["x"]`  
**Output**:  
`[["x"]]`

**Input**:  
`strs = [""]`  
**Output**:  
`[[""]]`

### Solution
```python
class Solution:
    def groupAnagrams(self, strs: list[str]) -> list[list[str]]:
        anagrams = {}
        for s in strs:
            key = ''.join(sorted(s))  
            # "act" "opst" "opst" "act" "opst" "aht"
            if key not in anagrams:
                anagrams[key] = []
            anagrams[key].append(s)
            #{"act":["act","cat"], "opst":["pots","tops","stop"],"aht":["hat"]}
        return list(anagrams.values())
```




### Top K Frequent Elements

Given an integer array nums and an integer k, return the k most frequent elements within the array.

The test cases are generated such that the answer is always unique.

You may return the output in any order.


Input: nums = [1,2,2,3,3,3], k = 2

Output: [2,3]
'

### Solution

```Python
from collections import Counter
class Solution:
    def topKFrequent(self, nums: List[int], k: int) -> List[int]: 
        if k==len(nums):
            return nums
        
        count=Counter(nums)
        # {3:6,4:2,1:1}
        return heapq.nlargest(k,count.keys(),key=count.get)

heapq.nlargest(k,count.keys(),key=count.get)
np.linspace(0,15,10)

from collections import Counter
class Solution:
    def topKFrequent(self, nums: List[int], k: int) -> List[int]: 
        if k==len(nums):
            return nums
        frequency={}
        for num in nums:
            if num in frequency:
                frequency[num]+=1
            else:
                frequency[num]=1
        # {3:6,4:2,1:1}
        sorted_keys = sorted(frequency, key=frequency.get, reverse=True)
        return sorted_keys[:k]
```