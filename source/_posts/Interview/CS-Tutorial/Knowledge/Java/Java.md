
---
tags: Interview
date: 2025-04-11 10:15:38
---


Java中println和print的区别：println一行输出之后可以自动换行，print不能

System.out对应的是System.err(报错提醒)


```Java
public class hello {
	public static void main(String[]arguments) { //void means no return value
		System.out.println("Hello World");//data type:boolean;int;double;String
		System.out.println("Hello World2");
		System.out.println("Number of arguments: " + arguments.length);
		// Check if any arguments are passed
        if (arguments.length == 0) {
            System.out.println("No arguments provided.");
        } else {
            System.out.println("Number of arguments: " + arguments.length);
            
            // Loop through the arguments array and print each argument
            for (int i = 0; i < arguments.length; i++) {
                System.out.println("Argument " + i + ": " + arguments[i]);
            }
        }
	}
}
```

// Java中，有且仅有double a = 5.0/2.0=2.5，其它都向下取整
int a=(int)18.7;