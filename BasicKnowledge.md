# BasicKnowledge
# Contents
[1.日期与问题](#questions)

[2.数据结构](#statics-structure)

[3.操作系统](#os)

[4.协议](#protocol)

[5.C/C++](#c-and-cpp)

[6.JAVA](#java)

[7.正则表达式](#regex)

[8.语言联想](#language)

## questions
- 3.21
    - 面试题: 进程与线程
    - C++: 宏
    - 数据结构: 单链表struct写
    - github markdown描点[](#)不支持中文标题  标题特殊符号C/C++
    
    
[返回目录](#contents)
## statics structure


[返回目录](#contents)
## os


[返回目录](#contents)
## protocol
- TCP三次握手、四次挥手
    - Seq(32 bit) ackNumber(32 bit) URG、ACK、PSH、RST、SYN、FIN(each 1 bit)
    - 三次握手：
    ```mermaid
    graph Shake3
    Client --> | SYN=1 Seq=random | --> Server
    Server --> | SYN=1 ACK=1 ackNumber=Seq+1 Seq1=random1 | --> Server
    Client --> | ACK=1 ackNumber=Seq1+1 | --> Server
    ```   
    <img src="pics/sh.png">
     
    - 四次挥手：
    ```mermaid
    graph Bye4
    Client --> | FIN=1 Seq=random | --> Server
    Server --> | ACK=1 ackNumber=Seq+1 Seq1=random1 | --> Server
    Server --> | FIN=1 | --> Client
    Client --> | ACK=1 ackNumber=Seq1+1 | --> Server    
    ```  
    <img src="pics/bye.png">
    
    
[返回目录](#contents)
## C AND CPP

[返回目录](#contents)
## JAVA

[返回目录](#contents)

## Regex
- 量词 贪婪 非贪婪
    - 量词
        - \* 0或n 
        - \+ 1或n
        - ? 0或1
        - {n} {n,} {n,m}        
    - 贪婪: 量词后不加? 表示从?前到匹配?后的串n次
    - 非贪婪: 量词后加? 表示从?前到匹配?后的串成功一次就不再继续
- 获取 非获取
    - 获取: (pat)
    - 非获取
        - str(?:pat)  str后匹配pat
        - str(?=pat)  str后匹配pat
        - (?<=pat)str  str前匹配pat
        - str(?!pat)  str后匹配pat
        - (?<!pat)str  str前匹配pat
        
- 元词
    - \b单词边界 \B
    - \w字母数字下划线 \W
    - \d数字 \D
    - \t制表符 \v垂直制表符 \n换行 \r回车 \f换页
    - \s任意空白符 \S
    - . 除\n \r的任意单字符
    
    
    
[返回目录](#contents)

## Language
- const final val 
    - 两种方式
        - eg(int a = 100 )
        - 声明后修改时就修改本内存的字面量(int a = 200 &a==#ffdfffff)
        - 声明后修改时重新开辟新内存字面量(int a = 200 &a==#dddddddd)
    - C++ Java Scala
        - C++： 变量 指针 引用
            - 变量： 对静态区的字面量的引用，eg（int a = 100）则a就是100
            - 指针： 对变量的地址的另储存eg（int *p = &a）则p就是一个存变量a的地址的变量p=#ffdfffff
            - 引用： 对变量的地址引用eg（int b = &a）则b就是a的地址的引用#ffdfffff  
    - var val: 指该引用所指的字面量是否可以改变
    - mutable immutable: 指其开辟的空间的字面量是否可以改变
        - 堆 栈 静态区
            - 堆： new关键字、构造器创建的大量的对象 对应整个内存中未被其他进程使用的乃至硬盘的虚拟内存
            - 栈： 一个基本数据类型的变量、一个对象的引用、函数调用的现场保存 操作起来最快但是很小
            - 静态区： 程序的字面量如“hello”、100等等
        - 堆 栈 队列
        - 普通变量
        - 数组 列表、Map、Set

[返回目录](#contents)
