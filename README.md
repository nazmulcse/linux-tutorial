# linux-tutorial
Basic tutorial of CentOS

### Useful Links

1. [Install LAMP (Linux Apache MySQL PHP) In CentOS 7](https://www.howtoforge.com/tutorial/centos-lamp-server-apache-mysql-php)

---

### Usefull linux(CentOS) command

```
systemctl start httpd.service               # Start Apache service
yum erase mysql-community-common.x86_64     # Remove mysql community 
yum install mariadb-server                  # Install mysql
yum install -y google-chrome-stable         # Install Google Chrome
yum install zip                             # Install ZIP
zip -r backup.zip /root/backup              # Make a ZIP folder. Here backup is folder in root

```
---

### How to install mysql connector java in centos 7
  First install mysql connector java in centos with following command
  `yum install mysql-connector-java`
  
  Then set class path for mysql connector with following command
  `export CLASSPATH=$CLASSPATH:/usr/share/java/mysql-connector-java.jar`
