## ubuntu 配置maven
- 从网络下载maven安装包[maven](http://maven.apache.org/download.cgi)
- 将得到的tar包解压到/opt/maven/
~~~
sudo mkdir /opt/maven/
sudo tar -zxvf  apache-maven-3.6.3-bin.tar.gz -C /opt/maven/
~~~

- 配置maven环境
~~~
sudo vim /etc/profile


在文档末尾写入：
## maven
export MAVEN_HOME=/opt/maven/apache-maven-3.6.3
export M2_HOME=$MAVEN_HOME
export CLASSPATH=$CLASSPATH:$MAVEN_HOME/lib
export PATH=$PATH:$MAVEN_HOME/bin

退出编辑，加载配置：
source /etc/profile
~~~
## ubuntu 配置gradle
