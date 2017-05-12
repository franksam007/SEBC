Run the Hadoop `p`i program as the user `chen`
<pre>export MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
export HADOOP=/opt/cloudera/parcels/CDH/bin
${HADOOP}/hadoop jar $MR/hadoop-examples.jar pi 4 100</pre>
><pre>Number of Maps  = 4
Samples per Map = 100
Wrote input for Map #0
Wrote input for Map #1
Wrote input for Map #2
Wrote input for Map #3
Starting Job
17/05/12 04:16:08 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-32-25.us-west-2.compute.internal/172.31.32.25:8032
17/05/12 04:16:08 INFO hdfs.DFSClient: Created token for chen: HDFS_DELEGATION_TOKEN owner=chen@FRANKSAM007.CN, renewer=yarn, realUser=, issueDate=1494562568849, maxDate=1495167368849, sequenceNumber=2, masterKeyId=2 on 172.31.32.25:8020
17/05/12 04:16:08 INFO security.TokenCache: Got dt for hdfs://ip-172-31-32-25.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.32.25:8020, Ident: (token for chen: HDFS_DELEGATION_TOKEN owner=chen@FRANKSAM007.CN, renewer=yarn, realUser=, issueDate=1494562568849, maxDate=1495167368849, sequenceNumber=2, masterKeyId=2)
17/05/12 04:16:09 INFO input.FileInputFormat: Total input paths to process : 4
17/05/12 04:16:09 INFO mapreduce.JobSubmitter: number of splits:4
17/05/12 04:16:09 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494561451439_0002
17/05/12 04:16:09 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.32.25:8020, Ident: (token for chen: HDFS_DELEGATION_TOKEN owner=chen@FRANKSAM007.CN, renewer=yarn, realUser=, issueDate=1494562568849, maxDate=1495167368849, sequenceNumber=2, masterKeyId=2)
17/05/12 04:16:09 INFO impl.YarnClientImpl: Submitted application application_1494561451439_0002
17/05/12 04:16:09 INFO mapreduce.Job: The url to track the job: http://ip-172-31-32-25.us-west-2.compute.internal:8088/proxy/application_1494561451439_0002/
17/05/12 04:16:09 INFO mapreduce.Job: Running job: job_1494561451439_0002
17/05/12 04:16:18 INFO mapreduce.Job: Job job_1494561451439_0002 running in uber mode : false
17/05/12 04:16:18 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 04:16:25 INFO mapreduce.Job:  map 25% reduce 0%
17/05/12 04:16:28 INFO mapreduce.Job:  map 50% reduce 0%
17/05/12 04:16:31 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 04:16:37 INFO mapreduce.Job:  map 100% reduce 100%
17/05/12 04:16:37 INFO mapreduce.Job: Job job_1494561451439_0002 completed successfully
17/05/12 04:16:37 INFO mapreduce.Job: Counters: 50
	File System Counters
		FILE: Number of bytes read=62
		FILE: Number of bytes written=621883
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=1188
		HDFS: Number of bytes written=215
		HDFS: Number of read operations=19
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=3
	Job Counters 
		Launched map tasks=4
		Launched reduce tasks=1
		Data-local map tasks=3
		Rack-local map tasks=1
		Total time spent by all maps in occupied slots (ms)=29284
		Total time spent by all reduces in occupied slots (ms)=4008
		Total time spent by all map tasks (ms)=29284
		Total time spent by all reduce tasks (ms)=4008
		Total vcore-seconds taken by all map tasks=29284
		Total vcore-seconds taken by all reduce tasks=4008
		Total megabyte-seconds taken by all map tasks=29986816
		Total megabyte-seconds taken by all reduce tasks=4104192
	Map-Reduce Framework
		Map input records=4
		Map output records=8
		Map output bytes=72
		Map output materialized bytes=136
		Input split bytes=716
		Combine input records=0
		Combine output records=0
		Reduce input groups=2
		Reduce shuffle bytes=136
		Reduce input records=8
		Reduce output records=0
		Spilled Records=16
		Shuffled Maps =4
		Failed Shuffles=0
		Merged Map outputs=4
		GC time elapsed (ms)=190
		CPU time spent (ms)=4130
		Physical memory (bytes) snapshot=1986203648
		Virtual memory (bytes) snapshot=7905374208
		Total committed heap usage (bytes)=2255486976
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=472
	File Output Format Counters 
		Bytes Written=97
Job Finished in 28.664 seconds
Estimated value of Pi is 3.17000000000000000000</pre>
