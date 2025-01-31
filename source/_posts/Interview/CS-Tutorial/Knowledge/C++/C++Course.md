


## Course 1: [Google Data Structures & Algorithms](https://techdevguide.withgoogle.com/paths/data-structures-and-algorithms/)


### Homework 1: Design a HashTable and HashMap

<div style="background-color: #f0f8ff; border: 2px solid #0078d7; padding: 15px; border-radius: 8px;">
  <h3 style="color: #0078d7;">Time Complexity</h3>
  <p>
  
(1) When the bucket size=1, the ***Insertion*** and ***Search*** are both ***O(1)***

(2) When the bucket size=N, the ***Insertion*** and ***Search*** are both ***O(N)***

(3) When the bucket size is too large,Hash uses height-balanced binary search tree: 
- average time complexity of insertion and search is O(1)
- the worst is O(logN) </p>
</div>




<br>

> bucket_index = hash(key) % backet_count = key % backet_count = 1

> Key could be *tuple*, *ingeger* and *string*

> If there is no *Hash Conflicts*,every value's *bucket_index* is different, the bucket size will be 1 

```C++

bucket_count = 10

print(hash(1) % bucket_count)  # 输出: 1
print(hash(11) % bucket_count) # 输出: 1
print(hash(21) % bucket_count) # 输出: 1
```


#### 2.HashTable

##### Exercise 1: Find the Duplicated Results


> hashTable.count(key)是用来判断是否存在的

> for (int key:nums),**key** is the first

```C++
class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        unordered_set<int> hashset;
        for (int key: nums){
            if (hashset.count(key)>0) {
                return true;
            }
            hashset.insert(key);
        }
        return false;
    }
};
```

```Python
class Solution(object):
    def containsDuplicate(self, nums):
        """
        :type nums: List[int]
        :rtype: bool
        """
        tank=set()
        for num in nums:
            if num in tank:
                return True
            tank.add(num)
        return False
```

##### Exercise 2:Given a non-empty array of integers nums, every element appears twice except for one. Find that single one.

> binary:二进制；XOR: exclusive OR
> - result^=nums ---- result=result^nums
> - nums^nums=0
> - nums^0=nums
> - x^y^z =(x^z)^y
> - XOR is under the binary calculation


```C++
#include <vector>
using namespace std;

class Solution {
public:
    int singleNumber(vector<int>& nums) {
        int result=0;
        for (int key : nums){
            result^=key;
        }
        return result;
        
    }
};
```

```Python
class Solution(object):
    def singleNumber(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        # 使用位运算 XOR 来解决问题
        result = 0
        for num in nums:
            result ^= num  # XOR 操作
        return result
```

##### Exercise 3: Given two integer arrays nums1 and nums2, return an array of their intersection. Each element in the result must be unique and you may return the result in any order.

Input: nums1 = [1,2,2,1], nums2 = [2,2]
Output: [2]

```Python
class Solution(object):
    def intersection(self, nums1, nums2):
        """
        :type nums1: List[int]
        :type nums2: List[int]
        :rtype: List[int]
        """
        num1=set(nums1)
        num2=set(nums2)
# Method 1:
#         for nu1 in num1:
#             if nu1 in num2:
#                 result.append(nu1)
#         return result

# Method 2:
        result= list(num1&num2)
        return result
```   

> *unordered_set<int>* set1 is the way to create the set in C++
- list1.push_back(key) is to add elements in list
- set1.insert(key) is to add elements in set
- set1.erase(key) is to delet elements in set/list


```C++
class Solution {
public:
    vector<int> intersection(vector<int>& nums1, vector<int>& nums2) {
        unordered_set<int> set1(nums1.begin(),nums1.end());
        unordered_set<int> set2(nums2.begin(),nums2.end());
        vector<int> result;
        for (int key: set1){
            if (set2.count(key)>0){
                result.push_back(key);
            }
        }
        return result;
    }
};

```

目前进度：
https://leetcode.com/explore/learn/card/hash-table/183/combination-with-other-algorithms/1131/
##### Exercise 4:




##### Exercise 5:Other Extensive Exercise

```Python
#include <unordered_set>
#include <iostream>
using namespace std;

int main() {
    unordered_set<int> hashset;

    cout << "The size of hash set is: " << hashset.size() << endl;

    for (auto it = hashset.begin(); it != hashset.end(); ++it) {
        cout << (*it) << " ";
    }
    cout << "are in the hash set." << endl;

    hashset.clear();

    if (hashset.empty()) {
        cout << "hash set is empty now!" << endl;
    }
}
```

#### 2. HashMap
```C++
class MyHashMap {
private:
    vector<int> hashMap;

public:
    MyHashMap() {
        // 初始化大小为 1000001 的数组，所有值设置为 -1（表示未映射）
        hashMap.resize(1000001, -1);
    }
    
    void put(int key, int value) {
        // 将指定 key 对应的值更新为 value
        hashMap[key] = value;
    }
    
    int get(int key) {
        // 如果 key 未被映射，返回 -1；否则返回对应的值
        return hashMap[key];
    }
    
    void remove(int key) {
        // 将指定 key 的映射值移除（设置为 -1）
        hashMap[key] = -1;
    }
};
```
 
> **Note:** private vs. public vs. protected

在 C++ 类中，访问权限有三种：
| 访问修饰符 | 作用                                  |
|------------|---------------------------------------|
| `private`  | 仅允许该类内部访问，外部不能访问或修改 |
| `protected`| 允许该类及其子类访问，但外部仍不能访问 |
| `public`   | 允许任何代码访问（不建议数据成员设为 `public`） |

```C++
class MyHashSet {
private:
    vector<bool> hashTable; // 只能通过add、remove、contains访问

public:
    MyHashSet() { hashTable.resize(1000001, false); }

    void add(int key) { hashTable[key] = true; }

    void remove(int key) { hashTable[key] = false; }

    bool contains(int key) { return hashTable[key]; }
};

int main() {
    MyHashSet mySet;
    mySet.add(5);
    
    // ❌ 不能访问 private 成员
    // cout << mySet.hashTable[5] << endl;  // 错误：'hashTable' 是 private
    
    cout << mySet.contains(5) << endl;  // ✅ 正确访问
}
```