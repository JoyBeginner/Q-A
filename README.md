<<<<<<< HEAD
# SparkHadoopScalaPythonTensorflow
recent job records

## maven
- maven sbt ant
- conf
  - settings.xml
  - respository
- pom.xml
  - spark : ${sparkscala.version}-${spark.version}
  - scala : ${scala.version} 

## hadoop
- namenode format
- web ui port : 50070
- hdfs fs -ls

## spark
- web ui port : 8080

### hadoop & spark & scala & jdk
- classpath?too much & findout why
- bin sbin
- start-all.sh
- conf
- hadoop fs -ls
18/04/10 19:45:48 WARN ipc.Client: Failed to connect to server: localhost/127.0.0.1:9000: try once and fail.
     - hadoop namenode -format
     - ./stop-all.sh
     - ./start-all.sh
- web ui
     - hadoop 50070 8088
     - spark 8080
     - 配置位置
- 之前一直报错connection refused,然后修改配置文件,不知道哪个起了作用
     - yarn-site.xml mapred-site.xml hdfs-site.xml core-site.xml hadoop-env.sh
     - 根据修改的配置新建了目录dirHadoop给nn snn dn使用
     
## python hdfs
- from Package import *
- import Package
    - 在包hdfs不一样,前者可以,后者找不到Client命名
 - jupyter notebook
    - shift+tab 查看函数方法   
    - 作图显示  %matplotlib inline   and   show()         
    - ax.view_init(elev=elev,azim=azim)#改变绘制图像的视角,即相机的位置,azim沿着z轴旋转，elev沿着y轴
    
## spark scala
- RDD交并补
    - 并集 ++
    - 交集
    - 补集
- RDD pairRDD String Char
    - RDD[String]
    - RDD[String,Int]
    - RDD[(String,Int)]
    - 
- 输出与预期不符时,先确定输出的是否是要输出的再找代码(逻辑)错误
- RDD输出去括号 bracket
- 细节问题
    - reduceByKey 
    - map 
    - flatMap 
    - split 
    - {} ()  
    - =>   
    - x(0)   x._1   
    - map换行、不换行
    - 字符串处理replaceAll 切片(python)等等
    
## python 
- 重载函数的问题
    - 类型重载
    - 个数重载（支持缺省参数）
        - eg func(a,b=0,c=0) 
        - 正确： func(1) func(1,'c') func(2,3,"hello")
    
=======
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
- tshark
    - 导出的包很大,输出的txt很小
    - sudo tshark -r jd_view_userA03241323_4.pcap -n -Y "ip.host contains \"jd\"" -T fields -e http.host 
        - solution: **su**
- idea 
    - invalid cache: 导致"cant solve symbol println"
- remarkable
    - ask for "install pygtkspellcheck" but err occurs "prob when import enchant" but enchant doesn't exist.
        - solved by pip install pyenchant.
- linux下
	- cmake : gcc -> make -> cmake
	- Makefile	
	- 命令 : c++  ld
	- 内核 
	- gtm
	- dkms
	- 写程序注意写每一步出错返回什么,让用程序的人好找到错误
	- 注意看程序的返回值,注重实践
	- .h .cpp std::isnan()
	    - 当使用<iostream.h>时，相当于在c中调用库函数，使用的是全局命名空间，也就是早期的c++实现；当使用<iostream>的时候，该头文件没有定义全局命名空间，必须使用namespace std
	
	
[返回目录](#contents)
## git
- push first time
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

- push second time
    - git init
    - git add -A(or .):A新增修改删除   .新增修改
    - git commit -m ./
    - git push -u origin *.git
    	- origin
    	    - git remote set-url --add origin: 向当前增加
    	    - git remote -v: 查看远程库信息
    -config:  git config -e  or  查看./git/config 

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
- strace 
    - 追踪命令交互过程
    - 标准输出
        - 0 stdin 
        - 1 stdout
        - 2 stderr
            - 2 > &1
- idea
    - ^q 查看方法的包及参数、返回数据类型
     
- jupyter notebook
    - shift+tab 查看函数方法   
    - 作图显示  %matplotlib inline   and   show()
      
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
- tensorflow
	- */anaconda2/bin/pip install --upgrade https://storage.googleapis.com/tensorflow/linux/cpu/tensorflow-1.1.0-cp27-none-linux_x86_64.whl
        

[返回目录](#contents)

