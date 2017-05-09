### Replicate to another cluster
---
* Source directory: franksam007
* Target directory: 
* Use `teragen` to create a 500 MB file
   `$ hadoop jar hadoop-examples-*.jar teragen 5000000 franksam007`
>17/05/09 03:36:32 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-33-107.us-west-2.compute.internal/172.31.33.107:8032  
17/05/09 03:36:33 INFO terasort.TeraSort: Generating 5000000 using 2  
17/05/09 03:36:33 INFO mapreduce.JobSubmitter: number of splits:2  
......  
	File Output Format Counters   
		Bytes Written=500000000  
* Copy your partner's file to your target directory
  * `distCp`  
   `$ hadoop distcp hdfs://ec2-52-39-45-145.us-west-2.compute.amazonaws.com:8020/user/hdfs/franksam007 hdfs://8020/user/hdfs/
* The results
  * Use `hdfs fsck <path> -files -blocks` on source and target directories  
  Source: `hdfs fsck /user/hdfs/franksam007 -files -blocks`  
>Connecting to namenode via http://ip-172-31-33-107.us-west-2.compute.internal:50070  
FSCK started by hdfs (auth:SIMPLE) from /172.31.44.106 for path /user/hdfs/franksam007 at Tue May 09 03:48:57 UTC 2017  
/user/hdfs/franksam007  
/user/hdfs/franksam007/_SUCCESS 0 bytes, 0 block(s):  OK  
/user/hdfs/franksam007/part-m-00000 250000000 bytes, 2 block(s):  OK  
>0. BP-1811825720-172.31.33.107-1494269172897:blk_1073743136_2312 len=134217728 Live_repl=3  
>1. BP-1811825720-172.31.33.107-1494269172897:blk_1073743138_2314 len=115782272 Live_repl=3  
>/user/hdfs/franksam007/part-m-00001 250000000 bytes, 2 block(s):  OK  
>0. BP-1811825720-172.31.33.107-1494269172897:blk_1073743137_2313 len=134217728 Live_repl=3  
>1. BP-1811825720-172.31.33.107-1494269172897:blk_1073743139_2315 len=115782272 Live_repl=3  
Status: HEALTHY  
 Total size:	500000000 B  
 Total dirs:	1  
 Total files:	3  
 Total symlinks:		0  
 Total blocks (validated):	4 (avg. block size 125000000 B)  
 Minimally replicated blocks:	4 (100.0 %)  
 Over-replicated blocks:	0 (0.0 %)  
 Under-replicated blocks:	0 (0.0 %)  
 Mis-replicated blocks:		0 (0.0 %)  
 Default replication factor:	3  
 Average block replication:	3.0  
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)  
 Number of data-nodes:		4  
 Number of racks:		1  
FSCK ended at Tue May 09 03:48:57 UTC 2017 in 3 milliseconds  
The filesystem under path '/user/hdfs/franksam007' is HEALTHY  

  target:  
