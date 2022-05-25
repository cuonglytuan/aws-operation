# Guide for install tomcat on linux2 server
## Java Install
```
yum install java-1.8.0-openjdk
```
## Port forwarding
### Edit `/etc/rc.d/rc.local`
```
vi /etc/rc.d/rc.local
```
With content
```
iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 8080  
iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 8443  
```
Apply change
```
chmod u+x /etc/rc.d/rc.local
systemctl start rc-local
```
## Tomcat Install
### Install from tar ball
```
wget https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.79/bin/apache-tomcat-8.5.79.tar.gz
tar -xvzf apache-tomcat-8.5.79.tar.gz
adduser tomcat
mv apache-tomcat-8.5.79 /home/tomcat/
chown -Rf tomcat.tomcat /home/tomcat/apache-tomcat-8.5.79
chmod 755 /home/tomcat/
ls -s /home/tomcat/apache-tomcat-8.5.79 ~root/tomcat8
```
### Export environment path
Edit `.bash_pprofile`
```
vi .bash_profile
```
with content
```
export CATALINA_HOME=/home/tomcat/apache-tomcat-8.5.79
export CATALINA_BASE=$CATALINA_HOME
```
apply change
```
source .bash_profile
```
### Configure tomcat start with instance
Add new file 
```
vi /etc/init.d/tomcat
```
with content
```
#!/bin/bash  
# description: Tomcat Start Stop Restart  
# processname: tomcat  
# chkconfig: 234 20 80  
CATALINA_HOME=/home/tomcat/apache-tomcat-8.5.79

case $1 in  
start)  
sh $CATALINA_HOME/bin/startup.sh  
;;   
stop)     
sh $CATALINA_HOME/bin/shutdown.sh  
;;   
restart)  
sh $CATALINA_HOME/bin/shutdown.sh  
sh $CATALINA_HOME/bin/startup.sh  
;;   
esac

```
apply change
```
chmod +x tomcat
chkconfig --add tomcat
chkconfig --level 234 tomcat on
chkconfig --list tomcat
```
