* What is ubertask optimization?  
   Ubertask optimization, which runs “sufficiently small” jobs sequentially within a single JVM, can be enbled by YARN Property "mapreduce.job.ubertask.enable"

* Where in CM is the Kerberos Security Realm value displayed?
   Settings/Kerberos

* Which CDH service(s) host a property for enabling Kerberos authentication?
   Zookeeper

* How do you upgrade the CM agents?
   Upgrape cloudera manager

* Give the tsquery statement used to chart Hue's CPU utilization?  
   `select cpu_system_rate + cpu_user_rate where category=ROLE and serviceName=hue`  

* Name all the roles that make up the Hive service  
   HiveServer2, Hive Metastore Server, Hive Gateway

* What steps must be completed before integrating Cloudera Manager with Kerberos?  
   Configure TLS encryption between Cloudera Manager Server and all Cloudera Manager Agent host systems