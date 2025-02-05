---

tags: Interview
date: 2023-09-11 10:15:38
---



### How to find the time
```C++
#include <iostream>
#include <ctime>

int main() {
    // Get the current time
    std::time_t now = std::time(nullptr);
    
    // Convert to local time
    std::tm* local_time = std::localtime(&now);

    // Output the formatted date
    std::cout << "Today's date: " 
              << (local_time->tm_year + 1900) << "-"  // Year (since 1900)
              << (local_time->tm_mon + 1) << "-"      // Month (0-based)
              << local_time->tm_mday                  // Day
              << std::endl;

    return 0;
}
```

### How to say Goodbye in different language?

```C++
using namespace std;
int main(){
 cout << "GoodBye~"<< endl;
 cout << "再见"<< endl;
 cout<<"안녕히 가세요" <<endl;
 cout<<"さようなら" <<endl;
 cout<<"Au revoir" <<endl;
 return 0;
}

```


### How to generate multiple lines

# include <iostream>
using namespace std;
int main(){
 cout<<"----------------------------------"<<endl;
 cout<<"|          x YES   NO x          |"<<endl;
 cout<<"|                                |"<<endl;
 cout<<"|         ABCDEFGHIJKLM          |"<<endl;
 cout<<"|         NOPQRSTUVWXYZ          |"<<endl;
 cout<<"|                                |"<<endl;
 cout<<"|           1234567890           |"<<endl;
 cout<<"----------------------------------"<<endl;
 return 0;
}


### Statements in C++

```C++
int main()
{
    int n = 1;  // declaration statement 声明语句
    n = n + 1;  // expression statement  表达式语句
    std::cout << "n = " << n << '\n'; // expression statement  表达式语句
    return 0;                         // return statement      返回语句
} 
```


### inputs in C++

```C++
#include <iostream>
using namespace std;

int main(){
 double Fahrenheit;
 double Celsius;

 cout<<"Please input the Fahrenheit:";
 cin>> Fahrenheit;

 Celsius= (Fahrenheit - 32) / 1.8;
 
 cout<< Celsius<<endl;
 return 0;
}
```

#### 多次输入
```C++
while (pin != 1234) { 
    std::cout << "Incorrect PIN. Enter your PIN again: "; 
    std::cin >> pin; 
  } 
```

### 换行符
```C++
#include <iostream>
using namespace std;

int main() {
    string name;
    
    // Ask for the name input
    cout << "Enter your name: ";
    cin >> name;
    
    // Output the chained sentences with newline after each one
    cout << "In the name of the Warrior, I charge you to be brave.\n"
         << "In the name of the Father, I charge you to be just.\n"
         << "In the name of the Mother, I charge you to defend the innocent.\n"
         << "Arise, " << name << ", a knight of the Seven Kingdoms." << endl;

    return 0;
}
```

### if 
```C++
if (cat>=3){

}else{

}
return 0;
```


### 随机数

```C++
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    srand(time(NULL));
    int randomNumber = rand() % 10; /*0-10之间的数*/；/*%2--0-1之间的数）
    cout << "Random number: " << randomNumber << endl;
    return 0;
}
```


### initialization 

#### Initialization 1
```C++
#include <iostream>
using namespace std;
int main() {
  for(int i=1;i<=2;i++){
    cout<<"sheep\n";
  }
  return 0;
}
```

#### Initialization 2
```C++
#include <iostream>
using namespace std;
int main() {
  for(int i=2;i>0;i--){
    cout<<i<< " bottles of beer on the wall\n"
    <<i<<" bottles of beer\n"
    <<"Take one down, pass it around\n"
    <<i-1<<" bottles of beer on the wall"<<endl;
  }
  return 0;
}
```