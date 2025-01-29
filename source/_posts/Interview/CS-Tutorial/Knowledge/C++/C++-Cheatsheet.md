
矩阵表达形式:

vector<string>;vector<int>

循环常用表达形式：

for (const string &word:components){
    cout<<word<< endl;
}

常见函数
```C++
list.pop_back()
set.insert()
list.erase()
set.erase()

stringSplit(v1,",")
stringToInterger(numstr)
intergerToString(num)
int randomnumber= randomInterger(1,100) //1-100
a.find("Apple")
if (a.find("p")!= string::npos){ // string::npos 表示未找到，不存在
    return 0;
}
```

```C++
int main(){
    string data="a,b,c";
    vector<string> components=stringSplit(data,",");
    for (const string & word: components){ // &表示引用而非拷贝；word表示元素；string对应之前容器中的元素类型
        cout<<word<<ednl;
    }
    return 0;
}

//【‘a','b','c'】
```

toLowerCase
```C++
int main(){
    string Data="ABC";
    cout << toLowerCase(Data)<<endl;
    return 0;
}
// "abc"
```


getLine
```C++
int main(){
    string input=getLine("Please Enter Here");
    cout <<"You Entered"<<input<<endl;
    return 0;
}
```


startsWith

```C++
int main(){
    string str="Hello World";
    if (startWith(str,"Hello")){
        cout<<"String starts with Hello"<<endl;
    }
    return 0;
}
```


一些规范表达：
header file 保护，如果已经定义过，即使重复也不能够调用

#ifndef EXAMPLE_H
#define EXAMPLE_H

// 头文件内容

#endif // EXAMPLE_H