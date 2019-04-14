# geowavelearning
https://locationtech.github.io/geowave/<br/>
http://lovrth.top/2018/10/06/GeoWave-%E5%8D%95%E6%9C%BA/<br/>
http://www.yanglajiao.com/article/sinat_35582093/80182019 <br/>
update-alternatives --list java<br/>
https://vimeo.com/238172796<br/>
https://vimeo.com/238173122<br/>

# hadoop
wget https://mirrors.tuna.tsinghua.edu.cn/apache/hadoop/common/hadoop-2.9.2/hadoop-2.9.2.tar.gz<br/>
tar zxvf hadoop-2.9.2.tar.gz<br/>

# zookeeper
wget http://mirror.bit.edu.cn/apache/zookeeper/zookeeper-3.4.14/zookeeper-3.4.14.tar.gz<br/>
sudo tar -zxf zookeeper-3.4.14.tar.gz -C /home/twl/  # 解压到/usr/local中<br/>
cd /home/twl/ <br/>
sudo chmod -R 777 zookeeper-3.4.14<br/>
vim /etc/profile
export ZK_HOME=/home/twl/zookeeper-3.4.14<br/>
export PATH=$PATH:$ZK_HOME/bin<br/>
source /etc/profile	    #修改生效<br/>

# hbase
wget http://mirror.bit.edu.cn/apache/hbase/1.4.9/hbase-1.4.9-bin.tar.gz<br/>
sudo tar -zxf hbase-1.4.9-bin.tar.gz -C /home/twl/ 
sudo chmod -R 777 hbase-1.4.9

export JAVA_HOME=/etc/alternatives/java_sdk_1.8.0_openjdk   #java路径
export HBASE_MANAGES_ZK=false       #不使用自带的zk

<property>
    <name>hbase.rootdir</name>
    <value>hdfs://localhost:9000/hbase/value>
</property>
<property>
    <name>hbase.cluster.distributed</name>
    <value>true</value>
</property>
<property>
    <name>hbase.zookeeper.property.dataDir</name>
    <value>/home/twl/zookeeper-3.4.14/datadir</value>
</property>
export HBASE_HOME=/home/twl/hbase-1.4.9
export PATH=$PATH:$HBASE_HOME/bin

sudo rpm -Uvh http://s3.amazonaws.com/geowave-rpms/release/noarch/geowave-repo-1.0-3.noarch.rpm

yum --enablerepo=geowave search geowave-0.9.8-apache-*

