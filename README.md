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
- jupyter notebook
    - jupyter notebook --generate-config
        - Overwrite ~/.jupyter/jupyter_notebook_config.py with default config? [y/N]n

     
     
[返回目录](#contents)
    
## config
- apache2 php7 mysql
    - apache2 apache2-mod-php7.0(note libapache2-mod-php7.0) php7.0 php7.0-mysql mysql-server mysql-client
    - config files:fpm/php.ini cli/php.ini apache2/conf.d
- Hadoop spark jdk scala
- sogou
    - fcitx fcitx-config-gtk fcitx-table-all im-swith(note im-config)
    - dpkg -i *.deb
- netease-cloud-music
    - dpkg -i *.deb
    - sudo apt install -f 
- pip
    - sudo -> undo
        - The directory '~/.cache/pip/http' or its parent directory is not owned by the current user and the cache has been disabled. Please check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's -H flag.
    - su -> do
    - pip install --upgrade pip
    - pip install jupyter notebook
    - **pip install --index https://mirrors.ustc.edu.cn/pypi/web/simple/ jupyter notebook**

[返回目录](#contents)
