

## 基础知识

private vs. public vs. protected

在 C++ 类中，访问权限有三种：
访问修饰符	作用
private	仅 允许该类内部访问，外部不能访问或修改
protected	允许该类 及其子类 访问，但外部仍不能访问
public	允许 任何代码 访问（不建议数据成员设为 public）

```python
Private:
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