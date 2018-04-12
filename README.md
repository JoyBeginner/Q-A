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
    