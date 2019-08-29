##Install openjdk 1.8.. & 11
   ```sh
   yum install java-1.8*
   #yum -y install java-1.8.0-openjdk-devel
   
   #sudo yum install java-11-openjdk-devel
   ```

##Confirm Java Version and set the java home
   ```sh
   java -version
   find /usr/lib/jvm/java-1.8* | head -n 3
   JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.212.b04-1.el8_0.x86_64
   export JAVA_HOME
   PATH=$PATH:$JAVA_HOME
    # To set it permanently update your .bash_profile
   vi ~/.bash_profile
   ```
   _The output should be something like this,_
    ```sh
   java -version
   openjdk version "1.8.0_151"
   OpenJDK Runtime Environment (build 1.8.0_151-b12)
   OpenJDK 64-Bit Server VM (build 25.151-b12, mixed mode)
   ```
OPEN JDK
```
yum install java-1.8.0-openjdk -y
yum install java-1.8.0-openjdk-devel -y

alternatives --config java
alternatives --config javac

JAVA_HOME="/usr/lib/jvm/open-jdk"
source /etc/environment
echo $JAVA_HOME
```
----------------------------------------------------------------------------------------------------------------------------------------
```
INSTALLING ORACLE JAVA(jdk-8u201)

LINK:-https://download.oracle.com/otn-pub/java/jdk/8u201-b09/42970487e3af4f5aa5bca3f542482c60/jdk-8u201-linux-x64.tar.gz

cd /opt

wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "https://download.oracle.com/otn-pub/java/jdk/8u201-b09/42970487e3af4f5aa5bca3f542482c60/jdk-8u201-linux-x64.tar.gz"

tar xzf jdk-8u201-linux-x64.tar.gz

cd /opt/jdk1.8.0_201/

alternatives --install /usr/bin/java java /opt/jdk1.8.0_201/bin/java 2
alternatives --config java


alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_201/bin/jar 2
alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_201/bin/javac 2
alternatives --set jar /opt/jdk1.8.0_201/bin/jar
alternatives --set javac /opt/jdk1.8.0_201/bin/javac


vi /etc/profile.d/java.sh

export JAVA_HOME=/opt/jdk1.8.0_201
export JRE_HOME=/opt/jdk1.8.0_201/jre
export PATH=$PATH:/opt/jdk1.8.0_201/bin:/opt/jdk1.8.0_201/jre/bin

source /etc/profile.d/java.sh
```
----------------------------------------------------------------------------------------------------------------------------------------
```
ORACLE JAVA(jdk1.8.0_191)
cd /opt/

yum install wget

wget --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "https://download.oracle.com/otn-pub/java/jdk/8u191-b12/2787e4a523244c269598db4e85c51e0c/jdk-8u191-linux-x64.tar.gz"

tar xzf jdk-8u191-linux-x64.tar.gz

cd /opt/jdk1.8.0_191/
alternatives --install /usr/bin/java java /opt/jdk1.8.0_191/bin/java 2
alternatives --config java

alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_191/bin/jar 2
alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_191/bin/javac 2
alternatives --set jar /opt/jdk1.8.0_191/bin/jar
alternatives --set javac /opt/jdk1.8.0_191/bin/javac

vi /etc/profile.d/java.sh


export JAVA_HOME=/opt/jdk1.8.0_191
export JRE_HOME=/opt/jdk1.8.0_191/jre
export PATH=$PATH:/opt/jdk1.8.0_181/bin:/opt/jdk1.8.0_191/jre/bin
source /etc/profile.d/java.sh

java -version
```
----------------------------------------------------------------------------------------------------------------------------------------
```
apt update
sudo apt-get install openjdk-8-jre
sudo apt-get install default-jre
sudo apt-get install default-jdk
sudo update-alternatives --config java
sudo apt-get install vim
sudo vim /etc/environment
JAVA_HOME="/usr/lib/jvm/java-8-oracle"
source /etc/environment
java -version
```
