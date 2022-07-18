https://www.cnblogs.com/-wenli/p/13273752.html
https://developer.aliyun.com/article/66204
https://juejin.cn/post/6995880612405968926
http://dblab.xmu.edu.cn/blog/2775-2/

# centos

* cd /opt/software
* wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u141-b15/336fa29ff2bb4ef291e347e091f7f4a7/jdk-8u141-linux-x64.tar.gz"
* wget http://archive.apache.org/dist/hadoop/common/hadoop-2.7.3/hadoop-2.7.3.tar.gz
* tar -zxvf hadoop-2.7.6.tar.gz -C /opt/apps/
* cd /opt/apps
* mv hadoop-2.7.6/ hadoop
* vim /ertc/hosts
* 



7057 ResourceManager
7347 Jps
2729 NodeManager
5722 JobHistoryServer
5805 NameNode
2381 DataNode

有时候一些服务起不来，把master 改成内网地址即可，参考https://cloud.tencent.com/developer/article/1084157?from=15425
网站无法访问的话，稍等一会
实例的出入站规则加下

http://dblab.xmu.edu.cn/blog/2775-2/
* hadoop jar /opt/apps/hadoop/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.3.jar grep /user/input output 'dfs[a-z.]+'
* hdfs dfs -mkdir -p /user/hadoop
* [root@iZa2d5hncdeacm4texaofeZ hadoop]# hdfs dfs -mkdir input
* hdfs dfs -put /opt/apps/hadoop/etc/hadoop/*.xml /user/input
*  hadoop jar ./share/hadoop/mapreduce/hadoop-mapreduce-examples-2.7.3.jar wordcount /input/input.txt /output
