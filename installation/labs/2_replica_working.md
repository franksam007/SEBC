===
#### MySQL installation
- - -
1. Implement the official MySQL repo   
   * Enable the repo to install MySQL 5.5  
`# cat /etc/yum.repos.d/mysql.repo`  
>`# MySQL 5.5`  
`[mysql55-community]`  
`name=MySQL 5.5 Community Server`  
`baseurl=http://repo.mysql.com/yum/mysql-5.5-community/el/6/$basearch/`  
`enabled=1`  
`gpgcheck=0` 
   * Install the `mysq`l package on all nodes   
`# yum install -y mysql-community-libs-compat`   
>`Loaded plugins: fastestmirror, presto`  
>`Loading mirror speeds from cached hostfile`
>`  * base: mirrors.xmission.com`  
>`  * extras: mirrors.unifiedlayer.com`  
>`  * updates: mirrors.tummy.com`  
>`mysql55-community                                                     | 2.5 kB     00:00`       
>`mysql55-community/primary_db                                          | 176 kB     00:00`     
>`Setting up Install Process`  
>`Resolving Dependencies`  
>`......`    
>`Installed:`  
`  mysql-community-libs.x86_64 0:5.5.56-2.el6`                                                  
`  mysql-community-libs-compat.x86_64 0:5.5.56-2.el6`                                            
`Dependency Installed:`  
`  mysql-community-common.x86_64 0:5.5.56-2.el6                                                ` 
`Replaced:`  
`  mysql-libs.x86_64 0:5.1.71-1.el6`  
`Complete!`
   * Install `mysql-server` on the server and replica nodes
  `# yum install mysql-community-server`  
>`Loaded plugins: fastestmirror, presto`  
>`Loading mirror speeds from cached hostfile`  
>` * base: repos.forethought.net`  
>` * extras: mirror.keystealth.org`  
>` * updates: centos.sonn.com`  
>`mysql55-community                                                     | 2.5 kB     00:00`     
>......  
>`Installed:`  
>`  mysql-community-server.x86_64 0:5.5.56-2.el6`  
`Dependency Installed:`  
`  libaio.x86_64 0:0.3.107-10.el6               mysql-community-client.x86_64 0:5.5.56-2.el6`  
`  perl.x86_64 4:5.10.1-144.el6                 perl-DBI.x86_64 0:1.609-4.el6`  
`  perl-Module-Pluggable.x86_64 1:3.90-144.el6  perl-Pod-Escapes.x86_64 1:1.04-144.el6`       
`  perl-Pod-Simple.x86_64 1:3.13-144.el6        perl-libs.x86_64 4:5.10.1-144.el6`            
`  perl-version.x86_64 3:0.77-144.el6`          
`Complete!`

   * Download and copy the JDBC connector to all node  
   `wget https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-5.1.42.tar.gz`
>......  
>`2017-05-08 13:35:26 (26.3 MB/s) - “mysql-connector-java-5.1.42.tar.gz” saved [3941920/3941920]`  

   `# ls /usr/share/java`  
>mysql-connector-java-5.1.42-bin.jar  mysql-connector-java.jar

2. Build a /etc/my.cnf file to start your MySQL server  
   On Master `/etc/my.cnf`
>[mysqld]  
log-bin=mysql-bin  
server-id=1  

   On Slave  `/etc/my.cnf`
>[mysqld]  
log-bin=mysql-bin  
server-id=2  
3. Start the mysqld service  
   `# service mysqld start`  
>Initializing MySQL database:  170508 14:13:09 [Note] Ignoring --secure-file-priv value as server is running with --bootstrap.  
......  
                                                           [  OK  ]  
Starting mysqld:                                           [  OK  ]  

   `# service mysqld status`
>mysqld (pid  2272) is running...

4. Use `/usr/bin/mysql_secure_installation`  
>NOTE: RUNNING ALL PARTS OF THIS SCRIPT IS RECOMMENDED FOR ALL MySQL  
      SERVERS IN PRODUCTION USE!  PLEASE READ EACH STEP CAREFULLY!  
>In order to log into MySQL to secure it, we'll need the current  
password for the root user.  If you've just installed MySQL, and  
you haven't set the root password yet, the password will be blank,  
so you should just press enter here.  
Enter current password for root (enter for none):   
OK, successfully used password, moving on...
Setting the root password ensures that nobody can log into the MySQL  
root user without the proper authorisation.  
Set root password? [Y/n] y  
......  
Reloading the privilege tables will ensure that all changes made so far  
will take effect immediately.  
Reload privilege tables now? [Y/n] y  
 ... Success!  
Cleaning up...
All done!  If you've completed all of the above steps, your MySQL   
installation should now be secure.  
Thanks for using MySQL!  
5. On the master MySQL node, grant replication privileges for your replica node:  
   `# mysql -u root --password='123456'`  
>mysql> CREATE USER 'repl'@'%' IDENTIFIED BY '123456';  
mysql> GRANT REPLICATION SLAVE ON *.* TO 'repl'@'%';  
mysql> SET GLOBAL binlog_format = 'ROW'  
mysql> FLUSH TABLES WITH READ LOCK;  
6. In a second terminal session, log into the MySQL master and show its status
   `mysql> SHOW MASTER STATUS;`
>+------------------+----------+--------------+------------------+  
| File             | Position | Binlog_Do_DB | Binlog_Ignore_DB |  
+------------------+----------+--------------+------------------+  
| mysql-bin.000001 |      226 |              |                  |  
+------------------+----------+--------------+------------------+  
1 row in set (0.00 sec)

   `mysql> UNLOCK TABLES;`  
>Query OK, 0 rows affected (0.00 sec)  

7.Login to the replica server and configure a connection to the master:
   `mysql> CHANGE MASTER TO MASTER_HOST='ec2-35-162-167-87.us-west-2.compute.amazonaws.com', MASTER_USER='repl', MASTER_PASSWORD='123456', MASTER_LOG_FILE='mysql-bin.000001', MASTER_LOG_POS=226;`  
8. Initiate slave operations on the replica  
   `mysql> START SLAVE;`
>Query OK, 0 rows affected (0.00 sec)  

   `mysql> SHOW SLAVE STATUS;`
>......
| Waiting for master to send event | ec2-35-162-167-87.us-west-2.compute.amazonaws.com |......
......

