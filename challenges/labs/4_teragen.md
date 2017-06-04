* The full `teragen` command and job output
```
export MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
export HADOOP=/opt/cloudera/parcels/CDH/bin
time ${HADOOP}/hadoop jar ${MR}/hadoop-examples.jar teragen \
                     -Ddfs.blocksize=64M \
                     -Dmapreduce.job.maps=6 \
                     -Dmapreduce.map.memory.mb=1024 \
                     -Dmapreduce.map.java.opts.max.heap=`echo "(1024*0.8)/1" | bc` \
                    65536000 tgen
```
```
17/05/12 03:27:10 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-32-25.us-west-2.compute.internal/172.31.32.25:8032
17/05/12 03:27:11 INFO terasort.TeraSort: Generating 65536000 using 6
17/05/12 03:27:11 INFO mapreduce.JobSubmitter: number of splits:6
17/05/12 03:27:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494557392473_0001
17/05/12 03:27:12 INFO impl.YarnClientImpl: Submitted application application_1494557392473_0001
17/05/12 03:27:12 INFO mapreduce.Job: The url to track the job: http://ip-172-31-32-25.us-west-2.compute.internal:8088/proxy/application_1494557392473_0001/
17/05/12 03:27:12 INFO mapreduce.Job: Running job: job_1494557392473_0001
17/05/12 03:27:20 INFO mapreduce.Job: Job job_1494557392473_0001 running in uber mode : false
17/05/12 03:27:20 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 03:27:33 INFO mapreduce.Job:  map 7% reduce 0%
17/05/12 03:27:34 INFO mapreduce.Job:  map 15% reduce 0%
17/05/12 03:27:36 INFO mapreduce.Job:  map 19% reduce 0%
17/05/12 03:27:38 INFO mapreduce.Job:  map 24% reduce 0%
17/05/12 03:27:40 INFO mapreduce.Job:  map 27% reduce 0%
17/05/12 03:27:41 INFO mapreduce.Job:  map 30% reduce 0%
17/05/12 03:27:43 INFO mapreduce.Job:  map 32% reduce 0%
17/05/12 03:27:44 INFO mapreduce.Job:  map 34% reduce 0%
17/05/12 03:27:46 INFO mapreduce.Job:  map 36% reduce 0%
17/05/12 03:27:47 INFO mapreduce.Job:  map 38% reduce 0%
17/05/12 03:27:49 INFO mapreduce.Job:  map 40% reduce 0%
17/05/12 03:27:50 INFO mapreduce.Job:  map 41% reduce 0%
17/05/12 03:27:52 INFO mapreduce.Job:  map 44% reduce 0%
17/05/12 03:27:55 INFO mapreduce.Job:  map 48% reduce 0%
17/05/12 03:27:58 INFO mapreduce.Job:  map 52% reduce 0%
17/05/12 03:28:01 INFO mapreduce.Job:  map 57% reduce 0%
17/05/12 03:28:04 INFO mapreduce.Job:  map 63% reduce 0%
17/05/12 03:28:07 INFO mapreduce.Job:  map 69% reduce 0%
17/05/12 03:28:11 INFO mapreduce.Job:  map 73% reduce 0%
17/05/12 03:28:14 INFO mapreduce.Job:  map 78% reduce 0%
17/05/12 03:28:17 INFO mapreduce.Job:  map 82% reduce 0%
17/05/12 03:28:20 INFO mapreduce.Job:  map 86% reduce 0%
17/05/12 03:28:22 INFO mapreduce.Job:  map 88% reduce 0%
17/05/12 03:28:23 INFO mapreduce.Job:  map 90% reduce 0%
17/05/12 03:28:25 INFO mapreduce.Job:  map 91% reduce 0%
17/05/12 03:28:26 INFO mapreduce.Job:  map 95% reduce 0%
17/05/12 03:28:28 INFO mapreduce.Job:  map 96% reduce 0%
17/05/12 03:28:29 INFO mapreduce.Job:  map 97% reduce 0%
17/05/12 03:28:30 INFO mapreduce.Job:  map 98% reduce 0%
17/05/12 03:28:32 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 03:28:32 INFO mapreduce.Job: Job job_1494557392473_0001 completed successfully
17/05/12 03:28:32 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=737304
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=511
		HDFS: Number of bytes written=6553600000
		HDFS: Number of read operations=24
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters 
		Launched map tasks=6
		Other local map tasks=6
		Total time spent by all maps in occupied slots (ms)=387134
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=387134
		Total vcore-seconds taken by all map tasks=387134
		Total megabyte-seconds taken by all map tasks=396425216
	Map-Reduce Framework
		Map input records=65536000
		Map output records=65536000
		Input split bytes=511
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=1248
		CPU time spent (ms)=124210
		Physical memory (bytes) snapshot=2010103808
		Virtual memory (bytes) snapshot=9420820480
		Total committed heap usage (bytes)=2030567424
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=140750829423462787
	File Input Format Counters 
		Bytes Read=0
	File Output Format Counters 
		Bytes Written=6553600000</pre>
```
* The result of the `time` command
```
real	1m24.774s
user	0m5.718s
sys	0m0.690s
```
* The command and output of `hdfs dfs -ls /user/zhou/tgen`  
```
Found 7 items
-rw-r--r--   3 zhou supergroup          0 2017-05-12 03:28 /user/zhou/tgen/_SUCCESS
-rw-r--r--   3 zhou supergroup 1092266700 2017-05-12 03:28 /user/zhou/tgen/part-m-00000
-rw-r--r--   3 zhou supergroup 1092266700 2017-05-12 03:28 /user/zhou/tgen/part-m-00001
-rw-r--r--   3 zhou supergroup 1092266600 2017-05-12 03:28 /user/zhou/tgen/part-m-00002
-rw-r--r--   3 zhou supergroup 1092266700 2017-05-12 03:28 /user/zhou/tgen/part-m-00003
-rw-r--r--   3 zhou supergroup 1092266700 2017-05-12 03:28 /user/zhou/tgen/part-m-00004
-rw-r--r--   3 zhou supergroup 1092266600 2017-05-12 03:28 /user/zhou/tgen/part-m-00005
```
