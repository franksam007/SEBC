1. The hostname of your db server node
>`# hostname -f`
>`ip-172-31-42-0.us-west-2.compute.internal
`
2. The command and output for display your database server's version
>`# mysql -V`
<pre>mysql  Ver 14.14 Distrib 5.6.36, for Linux (x86_64) using  EditLine wrapper
</pre>
3. The command and output for listing your created databases
><pre>mysql -u root --password='123456' -e "create user 'scm'@'%' identified by '123456'"
mysql -u root --password='123456' -e 'create database scm default character set utf8'
mysql -u root --password='123456' -e "grant all privileges on scm.* to 'scm'@'%'"
mysql -u root --password='123456' -e 'create database metastore default character set utf8;'
mysql -u root --password='123456' -e "CREATE USER 'hive'@'%' IDENTIFIED BY '123456'; create database hive default character set utf8; GRANT ALL PRIVILEGES ON hive.* TO 'hive'@'%';FLUSH PRIVILEGES;"
mysql -u root --password='123456' -e "create user 'rman'@'%' identified by '123456'"
mysql -u root --password='123456' -e 'create database rman default character set utf8'
mysql -u root --password='123456' -e "grant all privileges on rman.* to 'rman'@'%'"
mysql -u root --password='123456' -e "create user 'sentry'@'%' identified by '123456'"
mysql -u root --password='123456' -e 'create database sentry default character set utf8'
mysql -u root --password='123456' -e "grant all privileges on sentry.* to 'sentry'@'%'"
mysql -u root --password='123456' -e "create user 'hue'@'%' identified by '123456'"
mysql -u root --password='123456' -e 'create database hue default character set utf8'
mysql -u root --password='123456' -e "grant all privileges on hue.* to 'hue'@'%'"
mysql -u root --password='123456' -e "create user 'oozie'@'%' identified by '123456'"
mysql -u root --password='123456' -e 'create database oozie default character set utf8'
mysql -u root --password='123456' -e "grant all privileges on oozie.* to 'oozie'@'%'"</pre>
`mysql -u root --password='123456' -e 'SHOW DATABASES'`
><pre>+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| metastore          |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
</pre>