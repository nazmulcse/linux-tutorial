# linux-tutorial
Basic tutorial of CentOS

### Useful Links

1. [Install LAMP (Linux Apache MySQL PHP) In CentOS 7](https://www.howtoforge.com/tutorial/centos-lamp-server-apache-mysql-php)
2. [Make a Keyboard shortcut key for terminal In CentOS 7](https://stackoverflow.com/questions/26771044/how-do-i-make-a-keyboard-shortcut-for-terminal-in-centos-7)
3. [Make a Bootable Pendrive In CentOS 7](https://www.tecmint.com/install-linux-from-usb-device/)
4. [Install MySQL-Workbench In CentOS 7](https://www.linuxhelp.com/how-to-install-mysql-workbench-on-centos-7-new/)
5. [Start or Stop oracle service/database In CentOS 7](https://www.cyberciti.biz/faq/how-do-i-start-oracle-service-in-unix/)

---

### Usefull linux(CentOS) command

```
systemctl start httpd.service               # Start Apache service
systemctl start mariadb                     # Start MySQL/MariaDB service
yum erase mysql-community-common.x86_64     # Remove mysql community 
yum install mariadb-server                  # Install mysql
yum install -y google-chrome-stable         # Install Google Chrome
yum install zip                             # Install ZIP
zip -r backup.zip /root/backup              # Make a ZIP folder. Here backup is folder in root
tar zxvf /path/of/tar/file                  # Extract a tar file. Tar file extracted in current directory
yum clean all                               # Clean all metadata. If not work yum update command
nmtui                                       # Edit hostname and add static ip

```
---

### How to install mysql connector java in centos 7
  First install mysql connector java in centos with following command
  `yum install mysql-connector-java`
  
  Then set class path for mysql connector with following command
  `export CLASSPATH=$CLASSPATH:/usr/share/java/mysql-connector-java.jar`
  
  ---
  
  ### How to add an item(Quick Launch Icon) to the application menu in centos
    First create desktop file with application name by following command
    
    
    `vi /usr/share/applications/newitem.desktop    # Here newitem is application name`
      
    
    Add the following line in new window
    
    ```
    [Desktop Entry]
    Version=1.0
    Name=My Program
    Exec=/opt/eclipse/eclipse
    Terminal=false
    Type=Application
    StartupNotify=true
    Categories=Network;WebBrowser;
    X-Desktop-File-Install-Version=0.15
    ```
    
    Here `Name` is application name, `Categories` is the location in which category contain your application icon
