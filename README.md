# Q-A
Here is the PROBLEM&amp;SOLUTION I ever met.

## Tips
- jshell logout:
    - \exit
- scala logout:
    - :quit
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
    - 三次握手：
        
     
    - 四次挥手：
