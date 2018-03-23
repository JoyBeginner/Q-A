# Q-A
Here is the PROBLEM &amp; SOLUTION I ever met.
# contents
[1.Errors](#errors)

[2.git Cli](#git)

[3.技巧](#tips)

[4.安装与配置](#config)

## Errors
- [string "/usr/share/wireshark/init.lua"]:46: dofile has been disabled due to running Wireshark as superuser
    - 打开 /usr/share/wireshark/init.lua 文件
    - 将 dofile(DATA_DIR.."console.lua") 修改为 --dofile(DATA_DIR.."console.lua")
- wireshark https
    - SSLKEYLOGFILE
    - wireshark填写与$SSLKEYLOGFILE一致


[返回目录](#contents)
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
    - ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin
    - /etc/php/7.0/apache2/php.ini 
- Hadoop spark jdk scala
- sogou
    - fcitx fcitx-config-gtk fcitx-table-all im-swith(note im-config)
    - dpkg -i *.deb
- netease-cloud-music
    - dpkg -i *.deb
    - sudo apt install -f 
- pip
    - sudo -> undo
        - The directory '~/.cache/pip/http' or its parent directory is not owned by the current user and the cache has been
            disabled. Please check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's \              
            \-H flag.
    - su -> do
    - pip install --upgrade pip
    - pip install jupyter notebook
    - **pip install --index https://mirrors.ustc.edu.cn/pypi/web/simple/ jupyter notebook**
    - pip 超时
        [global]
        timeout = 6000
        index-url = http://e.pypi.python.org/simple
        [install]
        use-mirrors = true
        mirrors = http://e.pypi.python.org
- jupyter notebook 
    - 设置主目录: jupyter notebook --generate-config 
                Writing default config to: ~/.jupyter/jupyter_notebook_config.py
- idea jetbrains
    - 无法下载插件
    - 卸载重装
        - 删除目录
        - 删除~/.IdeaIC2017.3文件夹
        

[返回目录](#contents)
