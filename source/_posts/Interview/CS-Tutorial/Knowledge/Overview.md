
*<small>[Home](/About/index.html) > [Interview](/tags/Interview/index.html) > [CS Tutorial](/2023/09/11/Interview/CS-Tutorial/CS-Tutorial/index.html)> **[Knowledge](/2023/09/11/Interview/CS-Tutorial/Knowledge/Overview/index.html) </small>***



Hi,for this part, I will record the learning pace of myself about the following programming language.

### Content

- [C++](/2023/09/11/Interview/CS-Tutorial/Knowledge/C++/C++/index.html)
- [Java](/2023/09/11/Interview/CS-Tutorial/Knowledge/Java/Java/index.html)
- [Python](/2023/09/11/Interview/CS-Tutorial/Knowledge/Python/Python/index.html)
- [R](/2023/09/11/Interview/CS-Tutorial/Knowledge/R/R/index.html)
- [SQL](/2023/09/11/Interview/CS-Tutorial/Knowledge/SQL/SQL/index.html)


### Overview

> This page I will also write down some basic knowledge about the algo

- Curly Braces	{}	大括号
- Parentheses	()	小括号（圆括号）
- Square Brackets	[]	中括号
- Angle Brackets  <> 尖括号

#### 1.Data Structure

```Python
stack=Stack()
stack.push(1) #压入为顶元素
stack.pop() #弹出最后一个元素
#讲顺序，单一方向：先进先出

queue=Queue()
queue.append(1)#尾部加1
queue.popleft()#左端弹出
queue.pop()#右端弹出
#双向，讲顺序

bag=Bag()
bag.add(1)
bag.remove(1)
#不讲顺序
```

##### 2.2 Compile Langue

###### (1) java

- (从.java到.class):javac HelloWorld.java
- java -cp .. HW1.HelloWorld args[0] args[1] 
> HW1 为上层目录

###### (2) C++:  
- gcc helloWorld.c


#### 3.C++：

（1） 在C++中，我们经常在开始写代码之前加入：
using namespace std;
后续就可以只写：
cout << "This" << endl

（2） when to add Comma

*behind the non-control statement*

- **control statement**: if;while;switch;break;for——alter the program's flow

- **non-control statement**: variable declaration,assignment,function call——perform operation without affecting the flows

(3) forward declarations

```Python
void function2(int a, string b);
int function(int a, string b) {
function2(a, b); // now you can call this before writing
	return a + 2;    // function2
}
void function2(int a, string b) {
	cout << b << a + 2 << endl;
}
```




#### 4.Python


#### 5.Java



#### 6.SQL