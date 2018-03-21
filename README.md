# Q-A
Here is the PROBLEM&amp;SOLUTION I ever met.

## git
- push
    - git clone
    - git init
    - git add
    - git commit -m
    - git remote add origin *.git
        - *.git == git@github.com/*.git -> fatal:not a git respository **NOT SOLVED**
        - ssh -> already added.
            - **SOLVED**
            - git@github.com/*.git -> false
            - git@github.com:*.git -> right
    - git push -u origin master

## Tips
- jshell logout:
    - \exit
- scala logout:
    - :quit
- py logout
    - exit()
- wireshark SSLLOGFILE:
    - sudo -> false
    - su (open wireshark & browser in terminal) -> true
- update-alyernatives(run in super)
    - sudo update-alternatives --install /usr/bin/java java jvm/jdk1.8.0_162/bin/java 2
        - number means priority
    - sudo update-alternatives --config java
- ln -s
    - sudo ln -s src dst
- jdk8 jdk9 update-alternatives
    - ~/.bashrc 添加 JAVA_HOME CLASSPATH PATH(bin java) <- 设置PATH=$JAVA_PATH:$PATH
    - update-alternatives --config java <- 改变/usr/bin/java的指向
    - 结果:
    
        update-alternatives --config java 并不改变,因为先查在前的PATH
     

## 基础
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
    
## 安装与配置
- apache2 php7 mysql
    - apache2 apache2-mod-php7.0 php7.0 php7.0-mysql mysql-server mysql-client
    - config files:fpm/php.ini cli/php.ini apache2/conf.d
-Hadoop spark jdk scala
