1. The hostname of your db server node
>`# hostname -f`
>`ip-172-31-42-0.us-west-2.compute.internal
`
2. The command and output for display your database server's version
>`# mysql -V`
<pre>mysql  Ver 14.14 Distrib 5.6.36, for Linux (x86_64) using  EditLine wrapper
</pre>
3. The command and output for listing your created databases
>`mysql -u root --password='123456' -e 'SHOW DATABASES'`
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