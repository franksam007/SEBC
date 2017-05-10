* `curl -u franksam007:cloudera 'http://ec2-35-162-167-87.us-west-2.compute.amazonaws.com:7180/api/version'`  
v14
* `curl -u franksam007:cloudera 'http://ec2-35-162-167-87.us-west-2.compute.amazonaws.com:7180/api/v14/cm/version'`
<pre>{
  "version" : "5.9.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170112-1158",
  "gitHash" : "a66d8bbdbe8bc3ee54235e55423f2f76c7d9f3b1",
  "snapshot" : false
}</pre>
* `curl -u franksam007:cloudera 'http://ec2-35-162-167-87.us-west-2.compute.amazonaws.com:7180/api/v14/users'`
<pre>{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "franksam007",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}</pre>
* `curl -u franksam007:cloudera 'http://ec2-35-162-167-87.us-west-2.compute.amazonaws.com:7180/api/v14/cm/scmDbInfo'`
<pre>{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}</pre>