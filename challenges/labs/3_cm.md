* The command and output for `hdfs dfs -ls /user`  
   `# hdfs dfs -ls /user`
><pre>Found 7 items
drwxr-xr-x   - chen   supergroup          0 2017-05-12 03:02 /user/chen
drwxrwxrwx   - mapred hadoop              0 2017-05-12 02:49 /user/history
drwxrwxr-t   - hive   hive                0 2017-05-12 02:50 /user/hive
drwxrwxr-x   - hue    hue                 0 2017-05-12 02:51 /user/hue
drwxrwxr-x   - impala impala              0 2017-05-12 02:51 /user/impala
drwxrwxr-x   - oozie  oozie               0 2017-05-12 02:51 /user/oozie
drwxr-xr-x   - zhou   supergroup          0 2017-05-12 03:02 /user/zhou
</pre>
* The command and output from the CM API call ·`../api/v14/hosts`  
   `curl -u admin:admin 'http://ec2-34-210-151-78.us-west-2.compute.amazonaws.com:7180/api/v14/hosts'`
> <pre>{
  "items" : [ {
    "hostId" : "d81f7daa-5da0-4540-b7ea-bf74bd0efb95",
    "ipAddress" : "172.31.32.25",
    "hostname" : "ip-172-31-32-25.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/hostRedirect/d81f7daa-5da0-4540-b7ea-bf74bd0efb95",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "1522776e-f3ec-46b7-9e73-2745df15f18c",
    "ipAddress" : "172.31.40.91",
    "hostname" : "ip-172-31-40-91.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/hostRedirect/1522776e-f3ec-46b7-9e73-2745df15f18c",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "6c123404-4485-41ea-8d47-e1c8b7358191",
    "ipAddress" : "172.31.42.0",
    "hostname" : "ip-172-31-42-0.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/hostRedirect/6c123404-4485-41ea-8d47-e1c8b7358191",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "a66b6f6b-f1de-4c63-8706-763977415b34",
    "ipAddress" : "172.31.47.234",
    "hostname" : "ip-172-31-47-234.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/hostRedirect/a66b6f6b-f1de-4c63-8706-763977415b34",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  }, {
    "hostId" : "86c8479d-ac94-4f3a-82e4-77d31a8d7a71",
    "ipAddress" : "172.31.47.72",
    "hostname" : "ip-172-31-47-72.us-west-2.compute.internal",
    "rackId" : "/default",
    "hostUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/hostRedirect/86c8479d-ac94-4f3a-82e4-77d31a8d7a71",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "commissionState" : "COMMISSIONED",
    "numCores" : 4,
    "numPhysicalCores" : 4,
    "totalPhysMemBytes" : 15740305408
  } ]
}</pre>·
* The command and output from the CM API call `../api/v6/clusters/<githubName>/services`  
`curl -u admin:admin 'http://ec2-34-210-151-78.us-west-2.compute.amazonaws.com:7180/api/v6/clusters/franksam007/services'`
> <pre>{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "impala",
    "type" : "IMPALA",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/serviceRedirect/impala",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "IMPALA_ASSIGNMENT_LOCALITY",
      "summary" : "DISABLED"
    }, {
      "name" : "IMPALA_CATALOGSERVER_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_IMPALADS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "IMPALA_STATESTORE_HEALTH",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Impala"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://ip-172-31-47-72.us-west-2.compute.internal:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  } ]
</pre>