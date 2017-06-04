* Run the terasort program as `zhou` using the output target  
```
export MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
export HADOOP=/opt/cloudera/parcels/CDH/bin   
```
```
${HADOOP}/hadoop jar $MR/hadoop-examples.jar terasort \
                     tgen tsort
```    
<pre>17/05/12 04:06:34 INFO terasort.TeraSort: starting
17/05/12 04:06:36 INFO hdfs.DFSClient: Created token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@FRANKSAM007.CN, renewer=yarn, realUser=, issueDate=1494561996228, maxDate=1495166796228, sequenceNumber=1, masterKeyId=2 on 172.31.32.25:8020
17/05/12 04:06:36 INFO security.TokenCache: Got dt for hdfs://ip-172-31-32-25.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.32.25:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@FRANKSAM007.CN, renewer=yarn, realUser=, issueDate=1494561996228, maxDate=1495166796228, sequenceNumber=1, masterKeyId=2)
17/05/12 04:06:36 INFO input.FileInputFormat: Total input paths to process : 6
Spent 374ms computing base-splits.
Spent 5ms computing TeraScheduler splits.
Computing input splits took 380ms
Sampling 10 splits of 102
Making 8 from 100000 sampled records
Computing parititions took 850ms
Spent 1233ms computing partitions.
17/05/12 04:06:37 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-32-25.us-west-2.compute.internal/172.31.32.25:8032
17/05/12 04:06:37 INFO mapreduce.JobSubmitter: number of splits:102
17/05/12 04:06:38 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494561451439_0001
17/05/12 04:06:38 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.32.25:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@FRANKSAM007.CN, renewer=yarn, realUser=, issueDate=1494561996228, maxDate=1495166796228, sequenceNumber=1, masterKeyId=2)
17/05/12 04:06:38 INFO impl.YarnClientImpl: Submitted application application_1494561451439_0001
17/05/12 04:06:38 INFO mapreduce.Job: The url to track the job: http://ip-172-31-32-25.us-west-2.compute.internal:8088/proxy/application_1494561451439_0001/
17/05/12 04:06:38 INFO mapreduce.Job: Running job: job_1494561451439_0001
17/05/12 04:06:49 INFO mapreduce.Job: Job job_1494561451439_0001 running in uber mode : false
17/05/12 04:06:49 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 04:06:58 INFO mapreduce.Job:  map 1% reduce 0%
17/05/12 04:07:04 INFO mapreduce.Job:  map 4% reduce 0%
17/05/12 04:07:05 INFO mapreduce.Job:  map 8% reduce 0%
17/05/12 04:07:13 INFO mapreduce.Job:  map 9% reduce 0%
17/05/12 04:07:14 INFO mapreduce.Job:  map 13% reduce 0%
17/05/12 04:07:15 INFO mapreduce.Job:  map 15% reduce 0%
17/05/12 04:07:20 INFO mapreduce.Job:  map 16% reduce 0%
17/05/12 04:07:23 INFO mapreduce.Job:  map 18% reduce 0%
17/05/12 04:07:24 INFO mapreduce.Job:  map 22% reduce 0%
17/05/12 04:07:28 INFO mapreduce.Job:  map 23% reduce 0%
17/05/12 04:07:33 INFO mapreduce.Job:  map 25% reduce 0%
17/05/12 04:07:34 INFO mapreduce.Job:  map 26% reduce 0%
17/05/12 04:07:35 INFO mapreduce.Job:  map 29% reduce 0%
17/05/12 04:07:42 INFO mapreduce.Job:  map 32% reduce 0%
17/05/12 04:07:43 INFO mapreduce.Job:  map 34% reduce 0%
17/05/12 04:07:44 INFO mapreduce.Job:  map 36% reduce 0%
17/05/12 04:07:50 INFO mapreduce.Job:  map 37% reduce 0%
17/05/12 04:07:51 INFO mapreduce.Job:  map 40% reduce 0%
17/05/12 04:07:52 INFO mapreduce.Job:  map 41% reduce 0%
17/05/12 04:07:55 INFO mapreduce.Job:  map 43% reduce 0%
17/05/12 04:07:58 INFO mapreduce.Job:  map 44% reduce 0%
17/05/12 04:08:00 INFO mapreduce.Job:  map 47% reduce 0%
17/05/12 04:08:01 INFO mapreduce.Job:  map 48% reduce 0%
17/05/12 04:08:04 INFO mapreduce.Job:  map 50% reduce 0%
17/05/12 04:08:05 INFO mapreduce.Job:  map 51% reduce 0%
17/05/12 04:08:09 INFO mapreduce.Job:  map 54% reduce 0%
17/05/12 04:08:10 INFO mapreduce.Job:  map 55% reduce 0%
17/05/12 04:08:12 INFO mapreduce.Job:  map 56% reduce 0%
17/05/12 04:08:14 INFO mapreduce.Job:  map 58% reduce 0%
17/05/12 04:08:18 INFO mapreduce.Job:  map 61% reduce 0%
17/05/12 04:08:19 INFO mapreduce.Job:  map 62% reduce 0%
17/05/12 04:08:20 INFO mapreduce.Job:  map 63% reduce 0%
17/05/12 04:08:25 INFO mapreduce.Job:  map 65% reduce 0%
17/05/12 04:08:27 INFO mapreduce.Job:  map 70% reduce 0%
17/05/12 04:08:35 INFO mapreduce.Job:  map 73% reduce 0%
17/05/12 04:08:36 INFO mapreduce.Job:  map 75% reduce 0%
17/05/12 04:08:38 INFO mapreduce.Job:  map 76% reduce 0%
17/05/12 04:08:44 INFO mapreduce.Job:  map 77% reduce 0%
17/05/12 04:08:46 INFO mapreduce.Job:  map 82% reduce 0%
17/05/12 04:08:47 INFO mapreduce.Job:  map 83% reduce 0%
17/05/12 04:08:52 INFO mapreduce.Job:  map 84% reduce 0%
17/05/12 04:08:55 INFO mapreduce.Job:  map 89% reduce 0%
17/05/12 04:08:56 INFO mapreduce.Job:  map 90% reduce 0%
17/05/12 04:08:59 INFO mapreduce.Job:  map 91% reduce 0%
17/05/12 04:09:05 INFO mapreduce.Job:  map 92% reduce 3%
17/05/12 04:09:06 INFO mapreduce.Job:  map 93% reduce 6%
17/05/12 04:09:07 INFO mapreduce.Job:  map 93% reduce 10%
17/05/12 04:09:08 INFO mapreduce.Job:  map 93% reduce 12%
17/05/12 04:09:09 INFO mapreduce.Job:  map 93% reduce 19%
17/05/12 04:09:11 INFO mapreduce.Job:  map 94% reduce 19%
17/05/12 04:09:14 INFO mapreduce.Job:  map 95% reduce 19%
17/05/12 04:09:15 INFO mapreduce.Job:  map 95% reduce 20%
17/05/12 04:09:18 INFO mapreduce.Job:  map 96% reduce 20%
17/05/12 04:09:20 INFO mapreduce.Job:  map 97% reduce 20%
17/05/12 04:09:23 INFO mapreduce.Job:  map 98% reduce 20%
17/05/12 04:09:26 INFO mapreduce.Job:  map 99% reduce 20%
17/05/12 04:09:27 INFO mapreduce.Job:  map 99% reduce 21%
17/05/12 04:09:34 INFO mapreduce.Job:  map 99% reduce 25%
17/05/12 04:09:36 INFO mapreduce.Job:  map 99% reduce 29%
17/05/12 04:11:49 INFO mapreduce.Job:  map 99% reduce 25%
17/05/12 04:11:56 INFO mapreduce.Job:  map 100% reduce 25%
17/05/12 04:11:57 INFO mapreduce.Job:  map 100% reduce 27%
17/05/12 04:11:58 INFO mapreduce.Job:  map 100% reduce 39%
17/05/12 04:11:59 INFO mapreduce.Job:  map 100% reduce 48%
17/05/12 04:12:00 INFO mapreduce.Job:  map 100% reduce 50%
17/05/12 04:12:01 INFO mapreduce.Job:  map 100% reduce 53%
17/05/12 04:12:02 INFO mapreduce.Job:  map 100% reduce 54%
17/05/12 04:12:03 INFO mapreduce.Job:  map 100% reduce 55%
17/05/12 04:12:04 INFO mapreduce.Job:  map 100% reduce 58%
17/05/12 04:12:05 INFO mapreduce.Job:  map 100% reduce 60%
17/05/12 04:12:06 INFO mapreduce.Job:  map 100% reduce 61%
17/05/12 04:12:07 INFO mapreduce.Job:  map 100% reduce 64%
17/05/12 04:12:08 INFO mapreduce.Job:  map 100% reduce 70%
17/05/12 04:12:09 INFO mapreduce.Job:  map 100% reduce 71%
17/05/12 04:12:10 INFO mapreduce.Job:  map 100% reduce 73%
17/05/12 04:12:11 INFO mapreduce.Job:  map 100% reduce 75%
17/05/12 04:12:12 INFO mapreduce.Job:  map 100% reduce 76%
17/05/12 04:12:13 INFO mapreduce.Job:  map 100% reduce 79%
17/05/12 04:12:14 INFO mapreduce.Job:  map 100% reduce 83%
17/05/12 04:12:17 INFO mapreduce.Job:  map 100% reduce 85%
17/05/12 04:12:18 INFO mapreduce.Job:  map 100% reduce 89%
17/05/12 04:12:20 INFO mapreduce.Job:  map 100% reduce 90%
17/05/12 04:12:21 INFO mapreduce.Job:  map 100% reduce 95%
17/05/12 04:12:23 INFO mapreduce.Job:  map 100% reduce 96%
17/05/12 04:12:24 INFO mapreduce.Job:  map 100% reduce 97%
17/05/12 04:12:27 INFO mapreduce.Job:  map 100% reduce 98%
17/05/12 04:12:30 INFO mapreduce.Job:  map 100% reduce 100%
17/05/12 04:12:32 INFO mapreduce.Job: Job job_1494561451439_0001 completed successfully
17/05/12 04:12:32 INFO mapreduce.Job: Counters: 51
	File System Counters
		FILE: Number of bytes read=2932734654
		FILE: Number of bytes written=5819553462
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=6553614994
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=330
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=16
	Job Counters 
		Killed reduce tasks=1
		Launched map tasks=102
		Launched reduce tasks=9
		Data-local map tasks=101
		Rack-local map tasks=1
		Total time spent by all maps in occupied slots (ms)=837120
		Total time spent by all reduces in occupied slots (ms)=1334702
		Total time spent by all map tasks (ms)=837120
		Total time spent by all reduce tasks (ms)=1334702
		Total vcore-seconds taken by all map tasks=837120
		Total vcore-seconds taken by all reduce tasks=1334702
		Total megabyte-seconds taken by all map tasks=857210880
		Total megabyte-seconds taken by all reduce tasks=1366734848
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Map output bytes=6684672000
		Map output materialized bytes=2873054042
		Input split bytes=14994
		Combine input records=0
		Combine output records=0
		Reduce input groups=65536000
		Reduce shuffle bytes=2873054042
		Reduce input records=65536000
		Reduce output records=65536000
		Spilled Records=131072000
		Shuffled Maps =816
		Failed Shuffles=0
		Merged Map outputs=816
		GC time elapsed (ms)=13157
		CPU time spent (ms)=710060
		Physical memory (bytes) snapshot=58384384000
		Virtual memory (bytes) snapshot=173011955712
		Total committed heap usage (bytes)=67046473728
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters 
		Bytes Read=6553600000
	File Output Format Counters 
		Bytes Written=6553600000
17/05/12 04:12:32 INFO terasort.TeraSort: done</pre>
