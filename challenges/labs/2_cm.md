* List the command and output for `# ls /etc/yum.repos.d`
><pre>CentOS-Base.repo       CentOS-Media.repo  cm.repo
CentOS-Debuginfo.repo  CentOS-Vault.repo</pre>
* Use the `scm_prepare_database.sh` script to write your `db.properties` file
> `/usr/share/cmf/schema/scm_prepare_database.sh -h ip-172-31-42-0.us-west-2.compute.internal mysql scm scm 123456
JAVA_HOME=/usr/java/jdk1.7.0_67`
><pre>Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!</pre>
`