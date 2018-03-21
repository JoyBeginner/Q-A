# BasicKnowledge
# Contents
[1.日期与问题](#questions)

[2.数据结构](#statics-structure)

[3.操作系统](#os)

[4.协议](#protocol)

[5.C/C++](#C/C++)

[6.JAVA](#JAVA)

## questions
- 3.21
    - 面试题: 进程与线程
    - C++: 宏
    - 数据结构: 单链表struct写
    - github markdown描点[](#)不支持中文标题
## statics structure
## os
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
## C/C++
## JAVA
