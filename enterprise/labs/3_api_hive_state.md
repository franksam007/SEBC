* `curl -X POST -u franksam007:cloudera 'http://ec2-35-162-167-87.us-west-2.compute.amazonaws.com:7180/api/v2/clusters/Cluster1/services/hive/commands/stop'`
<pre>{
  "id" : 1067,
  "name" : "Stop",
  "startTime" : "2017-05-10T03:51:54.465Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}</pre>
* `curl -u admin:admin 'http://localhost:7180/api/v2/commands/1067'`
<pre>{
  "id" : 1067,
  "name" : "Stop",
  "startTime" : "2017-05-10T03:51:54.465Z",
  "endTime" : "2017-05-10T03:51:58.438Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully stopped service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 1068,
      "name" : "Stop",
      "startTime" : "2017-05-10T03:51:54.472Z",
      "endTime" : "2017-05-10T03:51:58.437Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-c7bc59f3f995d4a5d42569e2c9a5bb00"
      }
    }, {
      "id" : 1069,
      "name" : "Stop",
      "startTime" : "2017-05-10T03:51:54.475Z",
      "endTime" : "2017-05-10T03:51:58.419Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully stopped process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-c7bc59f3f995d4a5d42569e2c9a5bb00"
      }
    } ]
  }
}</pre>
* `curl -X POST -u franksam007:cloudera 'http://ec2-35-162-167-87.us-west-2.compute.amazonaws.com:7180/api/v2/clusters/Cluster1/services/hive/commands/start'`
<pre>{
  "id" : 1071,
  "name" : "Start",
  "startTime" : "2017-05-10T03:54:08.122Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}</pre>
* `curl -u admin:admin 'http://localhost:7180/api/v2/commands/1071'`
<pre>{
  "id" : 1071,
  "name" : "Start",
  "startTime" : "2017-05-10T03:54:08.122Z",
  "endTime" : "2017-05-10T03:54:30.933Z",
  "active" : false,
  "success" : true,
  "resultMessage" : "Successfully started service.",
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  },
  "children" : {
    "items" : [ {
      "id" : 1073,
      "name" : "Start",
      "startTime" : "2017-05-10T03:54:08.285Z",
      "endTime" : "2017-05-10T03:54:30.929Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVEMETASTORE-c7bc59f3f995d4a5d42569e2c9a5bb00"
      }
    }, {
      "id" : 1072,
      "name" : "Start",
      "startTime" : "2017-05-10T03:54:08.178Z",
      "endTime" : "2017-05-10T03:54:30.922Z",
      "active" : false,
      "success" : true,
      "resultMessage" : "Successfully started process.",
      "serviceRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive"
      },
      "roleRef" : {
        "clusterName" : "cluster",
        "serviceName" : "hive",
        "roleName" : "hive-HIVESERVER2-c7bc59f3f995d4a5d42569e2c9a5bb00"
      }
    } ]
  }
}</pre>