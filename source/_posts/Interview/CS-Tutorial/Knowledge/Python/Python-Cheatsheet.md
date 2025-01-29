
### (1)
sorted(s)-- ["o","p","s","t"]

> "".join -- "opst"

> list.index(value, start, end)


list.append()
set.add(/)
list.remove()
set.pop()

### (2) Data Model and dunder methods

| 操作符/行为   | 对应的魔法方法  | 示例            |
|---------------|----------------|-----------------|
| 加法 `+`      | `__add__`      | `vec1 + vec2`   |
| 减法 `-`      | `__sub__`      | `vec1 - vec2`   |
| 乘法 `*`      | `__mul__`      | `vec1 * vec2`   |
| 真除法 `/`    | `__truediv__`  | `vec1 / vec2`   |
| 地板除法 `//` | `__floordiv__` | `vec1 // vec2`  |
| 比较 `<`      | `__lt__`       | `vec1 < vec2`   |
| 比较 `==`     | `__eq__`       | `vec1 == vec2`  |


```python
class VectorND(object):
    def __init__(self, *args):
        """Create a VectorND from a sequence of real numbers."""
        self.values = list(args)

    def __len__(self):
        """Return the length of the vector."""
        return len(self.values)

    def __eq__(self, other):
        """Check if the vector is equal to another."""
        if not isinstance(other, VectorND):
            return False
        return self.values == other.values

    def __add__(self, other):
        """Add two VectorND objects and return a new VectorND."""
        if len(self) != len(other):
            raise ValueError("vector lengths are incompatible")
        return VectorND(*(a + b for a, b in zip(self.values, other.values)))

    def __sub__(self, other):
        """Subtract one VectorND object from another."""
        if len(self) != len(other):
            raise ValueError("vector lengths are incompatible")
        return VectorND(*(a - b for a, b in zip(self.values, other.values)))

    def __repr__(self):
        """Output the "official" string representation of the object."""
        return f"Vector: {self.values}"

# Example usage
vec1 = VectorND(1, 2, 3)
vec2 = VectorND(4, 5, 6)
print(vec1+ vec2)  # Output: Vector: [5, 7, 9]
print(vec1 - vec2)  # Output: Vector: [-3, -3, -3]
print(len(vec1))    # Output: 3
print(vec1 == vec2) # Output: False


return f"Vector:{self.values}"
```

### (3) Matrix Operation

```python
binv = np.linalg.inv(b) #逆矩阵
binv = np.linalg.det(b) #行列式
binv = np.linalg.eig(b) #特征值
binv = np.linalg.svd(b) #奇异值分解，U∑V;奇异值=特征V值的开方
np.linspace(0,15,10) 
```

### (4) DataFrame Operation

```Python
df.iloc[2] # 第三行
df.loc['1'] #以1作为index的那一行
df.loc[['2','3'],'h'] #2,3作为index同时h作为列的数据
df = pd.DataFrame(np.random.randn(3,3),index='1 2 3'.split(),columns='1 2 3'.split()) #randn 是正态分布



```