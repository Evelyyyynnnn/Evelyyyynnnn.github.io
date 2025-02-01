---
tags: Interview
date: 2023-09-11 10:15:38
---

*<small>[Home](/About/index.html) > [Interview](/tags/Interview/index.html) > [CS Tutorial](/2023/09/11/Interview/CS-Tutorial/CS-Tutorial/index.html)> **[Knowledge](/2023/09/11/Interview/CS-Tutorial/Knowledge/Overview/index.html) </small>***



Hi,for this part, I will record the learning pace of myself about the following programming language.

## Content

- [C++](/2023/09/11/Interview/CS-Tutorial/Knowledge/C++/C++/index.html)
- [Java](/2023/09/11/Interview/CS-Tutorial/Knowledge/Java/Java/index.html)
- [Python](/2023/09/11/Interview/CS-Tutorial/Knowledge/Python/Python/index.html)
- [R](/2023/09/11/Interview/CS-Tutorial/Knowledge/R/R/index.html)
- [SQL](/2023/09/11/Interview/CS-Tutorial/Knowledge/SQL/SQL/index.html)


## Overview

> This page I will also write down some basic knowledge about the algo

- Curly Braces	{}	大括号
- Parentheses	()	小括号（圆括号）
- Square Brackets	[]	中括号
- Angle Brackets  <> 尖括号



### 1. java

- (从.java到.class):javac HelloWorld.java
- java -cp .. HW1.HelloWorld args[0] args[1] 
> HW1 为上层目录

### 2. C++:  
- gcc helloWorld.c


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




### 3.Python


### 4.Java



### 5.SQL