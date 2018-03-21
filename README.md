# Q-A
Here is the PROBLEM&amp;SOLUTION I ever met.
# contents

[1.git Cli](#git)

[2.技巧](#tips)

[3.安装与配置](#config)

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


[返回目录](#contents)
## Tips
- jshell logout:
    - \exit
- scala logout:
    - :quit
- py logout
    - exit()
- ssh-keygen -t rsa -C "your_email@example.com"
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
     
     
[返回目录](#contents)
    
## config
- apache2 php7 mysql
    - apache2 apache2-mod-php7.0 php7.0 php7.0-mysql mysql-server mysql-client
    - config files:fpm/php.ini cli/php.ini apache2/conf.d
- Hadoop spark jdk scala

[返回目录](#contents)
