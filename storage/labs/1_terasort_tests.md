### Test HDFS throughput
1. Create an end-user Linux account named with GitHub handle  
   * `useradd franksam007` at all hosts  
   * Create an HDFS directory under /user  
   `$ hdfs dfs -mkdir /user/franksam007`  
   `$ hdfs dfs -chown franksam007 /user/franksam007`  
2. Create a 10 GB file using `teragen`  
   `$time hadoop jar hadoop-examples-*.jar teragen -D mapreduce.job.maps=4 -D dfs.block.size=33554432 100000000 teragen1`  
>17/05/09 13:44:54 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-107.us-west-2.compute.internal/172.31.33.107:8032  
17/05/09 13:44:55 INFO terasort.TeraSort: Generating 100000000 using 4  
17/05/09 13:44:55 INFO mapreduce.JobSubmitter: number of splits:4  
17/05/09 13:44:55 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize  
17/05/09 13:44:55 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494322386818_0002  
17/05/09 13:44:56 INFO impl.YarnClientImpl: Submitted application application_1494322386818_0002  
17/05/09 13:44:56 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-107.us-west-2.compute.internal:8088/proxy/application_1494322386818_0002/  
17/05/09 13:44:56 INFO mapreduce.Job: Running job: job_1494322386818_0002  
17/05/09 13:45:02 INFO mapreduce.Job: Job job_1494322386818_0002 running in uber mode : false
17/05/09 13:45:02 INFO mapreduce.Job:  map 0% reduce 0%  
......  
17/05/09 13:47:13 INFO mapreduce.Job:  map 100% reduce 0%  
17/05/09 13:47:13 INFO mapreduce.Job: Job job_1494322386818_0002 completed successfully  
17/05/09 13:47:13 INFO mapreduce.Job: Counters: 32  
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=499436  
		FILE: Number of read operations=0  
		FILE: Number of large read operations=0  
		FILE: Number of write operations=0  
		HDFS: Number of bytes read=344  
		HDFS: Number of bytes written=10000000000  
		HDFS: Number of read operations=16  
		HDFS: Number of large read operations=0  
		HDFS: Number of write operations=8  
	Job Counters 
		Killed map tasks=2  
		Launched map tasks=6  
		Other local map tasks=6  
		Total time spent by all maps in occupied slots (ms)=484082  
		Total time spent by all reduces in occupied slots (ms)=0  
		Total time spent by all map tasks (ms)=484082  
		Total vcore-seconds taken by all map tasks=484082  
		Total megabyte-seconds taken by all map tasks=495699968  
	Map-Reduce Framework  
		Map input records=100000000  
		Map output records=100000000  
		Input split bytes=344   
		Spilled Records=0  
		Failed Shuffles=0  
		Merged Map outputs=0  
		GC time elapsed (ms)=1982  
		CPU time spent (ms)=171260  
		Physical memory (bytes) snapshot=824537088  
		Virtual memory (bytes) snapshot=6260359168  
		Total committed heap usage (bytes)=887095296  
	org.apache.hadoop.examples.terasort.TeraGen$Counters  
		CHECKSUM=214760662691937609  
	File Input Format Counters  
		Bytes Read=0  
	File Output Format Counters  
		Bytes Written=10000000000  
real	2m16.902s  
user	0m6.052s  
sys	0m0.835s  

`$time hadoop jar hadoop-examples-*.jar terasort /user/franksam007/teragen1 /user/franksam007/terasort1`   
>17/05/09 06:01:59 INFO terasort.TeraSort: starting  
17/05/09 06:02:01 INFO input.FileInputFormat: Total input paths to process : 2  
Spent 327ms computing base-splits.  
Spent 6ms computing TeraScheduler splits.  
Computing input splits took 334ms  
Sampling 10 splits of 298  
Making 8 from 100000 sampled records  
Computing parititions took 914ms  
Spent 1250ms computing partitions.  
17/05/09 06:02:02 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-107.us-west-2.compute.internal/172.31.33.107:8032  
17/05/09 06:02:02 INFO mapreduce.JobSubmitter: number of splits:298  
17/05/09 06:02:02 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize  
17/05/09 06:02:03 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494271886278_0008  
17/05/09 06:02:03 INFO impl.YarnClientImpl: Submitted application application_1494271886278_0008  
17/05/09 06:02:03 INFO mapreduce.Job: The url to track the job: http://ip-172-31-33-107.us-west-2.compute.internal:8088/proxy/application_1494271886278_0008/  
17/05/09 06:02:03 INFO mapreduce.Job: Running job: job_1494271886278_0008
17/05/09 06:02:09 INFO mapreduce.Job: Job job_1494271886278_0008 running in uber mode : false  
17/05/09 06:02:09 INFO mapreduce.Job:  map 0% reduce 0%  
......
17/05/09 06:06:46 INFO mapreduce.Job:  map 83% reduce 0%  
17/05/09 06:06:53 INFO mapreduce.Job:  map 84% reduce 0%  
17/05/09 06:06:56 INFO mapreduce.Job:  map 84% reduce 8%  
17/05/09 06:07:00 INFO mapreduce.Job:  map 84% reduce 9%  
17/05/09 06:07:02 INFO mapreduce.Job:  map 85% reduce 9%  
17/05/09 06:07:03 INFO mapreduce.Job:  map 85% reduce 11%  
......  
17/05/09 06:09:11 INFO mapreduce.Job:  map 100% reduce 99%  
17/05/09 06:09:14 INFO mapreduce.Job:  map 100% reduce 100%  
17/05/09 06:09:15 INFO mapreduce.Job: Job job_1494271886278_0008 completed successfully  
17/05/09 06:09:15 INFO mapreduce.Job: Counters: 50  
	File System Counters  
		FILE: Number of bytes read=4477476573  
		FILE: Number of bytes written=8890597087  
		FILE: Number of read operations=0  
		FILE: Number of large read operations=0  
		FILE: Number of write operations=0  
		HDFS: Number of bytes read=10000047382  
		HDFS: Number of bytes written=10000000000  
		HDFS: Number of read operations=918  
		HDFS: Number of large read operations=0  
		HDFS: Number of write operations=16  
	Job Counters  
		Launched map tasks=298  
		Launched reduce tasks=8  
		Data-local map tasks=297  
		Rack-local map tasks=1  
		Total time spent by all maps in occupied slots (ms)=1981987  
		Total time spent by all reduces in occupied slots (ms)=549654  
		Total time spent by all map tasks (ms)=1981987  
		Total time spent by all reduce tasks (ms)=549654  
		Total vcore-seconds taken by all map tasks=1981987  
		Total vcore-seconds taken by all reduce tasks=549654  
		Total megabyte-seconds taken by all map tasks=2029554688  
		Total megabyte-seconds taken by all reduce tasks=562845696  
	Map-Reduce Framework  
		Map input records=100000000  
		Map output records=100000000  
		Map output bytes=10200000000  
		Map output materialized bytes=4374987782  
		Input split bytes=47382  
		Combine input records=0  
		Combine output records=0  
		Reduce input groups=100000000  
		Reduce shuffle bytes=4374987782  
		Reduce input records=100000000  
		Reduce output records=100000000  
		Spilled Records=200000000  
		Shuffled Maps =2384  
		Failed Shuffles=0  
		Merged Map outputs=2384  
		GC time elapsed (ms)=25736  
		CPU time spent (ms)=1368680  
		Physical memory (bytes) snapshot=145123467264  
		Virtual memory (bytes) snapshot=478945878016  
		Total committed heap usage (bytes)=174555922432  
	Shuffle Errors  
		BAD_ID=0  
		CONNECTION=0  
		IO_ERROR=0  
		WRONG_LENGTH=0  
		WRONG_MAP=0  
		WRONG_REDUCE=0  
	File Input Format Counters  
		Bytes Read=10000000000  
	File Output Format Counters  
		Bytes Written=10000000000  
17/05/09 06:09:15 INFO terasort.TeraSort: done  
real	7m16.819s  
user	0m9.747s  
sys	0m1.023s  

