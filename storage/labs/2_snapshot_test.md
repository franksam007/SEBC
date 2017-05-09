* Create a `precious` directory in HDFS; copy the ZIP course file into it
   `$ hdfs dfs -mkdir /user/hdfs/precious`  
   `$ hdfs dfs -put /opt/tool/SEBC-Shanghai.zip /user/hdfs/precious`  
   `$ hdfs dfs -ls /user/hdfs/precious`  
>Found 1 items  
-rw-r--r--   3 hdfs supergroup     474957 2017-05-09 06:55 /user/hdfs/precious/SEBC-Shanghai.zip
* Enable snapshots for `precious` 
   `$ hdfs dfsadmin -allowSnapshot /user/hdfs/precious`  
>Allowing snaphot on /user/hdfs/precious succeeded  \

   `$ hdfs lsSnapshottableDir`  
>drwxr-xr-x 0 hdfs supergroup 0 2017-05-09 07:05 1 65536 /user/hdfs/precious  
* Create a snapshot called `sebc-hdfs-test`  
   `$ hdfs dfs -createSnapshot /user/hdfs/precious sebc-hdfs-test`  
>Created snapshot /user/hdfs/precious/.snapshot/sebc-hdfs-test
* Delete the directory
   `$ hdfs dfs -rm -r /user/hdfs/precious `
>rm: Failed to move to trash: hdfs://ip-172-31-33-107.us-west-2.compute.internal:8020/user/hdfs/precious: The directory /user/hdfs/precious cannot be deleted since /user/hdfs/precious is snapshottable and already has snapshots  
* Delete the ZIP file
   `$ hdfs dfs -rm /user/hdfs/precious/SEBC-Shanghai.zip`  
>17/05/09 07:48:36 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-33-107.us-west-2.compute.internal:8020/user/hdfs/precious/SEBC-Shanghai.zip' to trash at: hdfs://ip-172-31-33-107.us-west-2.compute.internal:8020/user/hdfs/.Trash/Current/user/hdfs/precious/SEBC-Shanghai.zip  
* Restore the deleted file  
   `hadoop distcp /user/hdfs/precious/.snapshot/sebc-hdfs-test/SEBC-Shanghai.zip /user/hdfs/precious/`   
>17/05/09 08:13:04 INFO tools.DistCp: Input Options: DistCpOptions{atomicCommit=false, syncFolder=false, deleteMissing=false, ignoreFailures=false, overwrite=false, append=false, useDiff=false, useRdiff=false, fromSnapshot=null, toSnapshot=null, skipCRC=false, blocking=true, numListstatusThreads=0, maxMaps=20, mapBandwidth=100, sslConfigurationFile='null', copyStrategy='uniformsize', preserveStatus=[], preserveRawXattrs=false, atomicWorkPath=null, logPath=null, sourceFileListing=null, sourcePaths=[/user/hdfs/precious/.snapshot/sebc-hdfs-test/SEBC-Shanghai.zip], targetPath=/user/hdfs/precious, targetPathExists=true, filtersFile='null'}  
......  
	org.apache.hadoop.tools.mapred.CopyMapper$Counter  
		BYTESCOPIED=474957  
		BYTESEXPECTED=474957  
		COPY=1  