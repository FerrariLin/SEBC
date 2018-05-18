## command
```
[groot@ip-172-31-81-26 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen  -Ddfs.block.size=64000000 -Dmapreduce.job.maps=40 -Dmapreduce.map.memory.mb=1024 50000000 /user/groot/tgen
18/05/18 05:14:11 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-87-98.ec2.internal/172.31.87.98:8032
18/05/18 05:14:11 INFO terasort.TeraGen: Generating 50000000 using 40
18/05/18 05:14:11 INFO mapreduce.JobSubmitter: number of splits:40
18/05/18 05:14:11 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/18 05:14:11 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526617839979_0006
18/05/18 05:14:12 INFO impl.YarnClientImpl: Submitted application application_1526617839979_0006
18/05/18 05:14:12 INFO mapreduce.Job: The url to track the job: http://ip-172-31-87-98.ec2.internal:8088/proxy/application_1526617839979_0006/
18/05/18 05:14:12 INFO mapreduce.Job: Running job: job_1526617839979_0006
18/05/18 05:14:18 INFO mapreduce.Job: Job job_1526617839979_0006 running in uber mode : false
18/05/18 05:14:18 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 05:14:25 INFO mapreduce.Job:  map 3% reduce 0%
18/05/18 05:14:27 INFO mapreduce.Job:  map 8% reduce 0%
18/05/18 05:14:28 INFO mapreduce.Job:  map 10% reduce 0%
18/05/18 05:14:29 INFO mapreduce.Job:  map 13% reduce 0%
18/05/18 05:14:32 INFO mapreduce.Job:  map 15% reduce 0%
18/05/18 05:14:35 INFO mapreduce.Job:  map 20% reduce 0%
18/05/18 05:14:37 INFO mapreduce.Job:  map 25% reduce 0%
18/05/18 05:14:39 INFO mapreduce.Job:  map 28% reduce 0%
18/05/18 05:14:43 INFO mapreduce.Job:  map 30% reduce 0%
18/05/18 05:14:44 INFO mapreduce.Job:  map 32% reduce 0%
18/05/18 05:14:45 INFO mapreduce.Job:  map 38% reduce 0%
18/05/18 05:14:46 INFO mapreduce.Job:  map 40% reduce 0%
18/05/18 05:14:51 INFO mapreduce.Job:  map 43% reduce 0%
18/05/18 05:14:52 INFO mapreduce.Job:  map 47% reduce 0%
18/05/18 05:14:53 INFO mapreduce.Job:  map 50% reduce 0%
18/05/18 05:14:55 INFO mapreduce.Job:  map 52% reduce 0%
18/05/18 05:14:57 INFO mapreduce.Job:  map 55% reduce 0%
18/05/18 05:15:00 INFO mapreduce.Job:  map 60% reduce 0%
18/05/18 05:15:01 INFO mapreduce.Job:  map 63% reduce 0%
18/05/18 05:15:04 INFO mapreduce.Job:  map 68% reduce 0%
18/05/18 05:15:08 INFO mapreduce.Job:  map 70% reduce 0%
18/05/18 05:15:09 INFO mapreduce.Job:  map 73% reduce 0%
18/05/18 05:15:10 INFO mapreduce.Job:  map 75% reduce 0%
18/05/18 05:15:12 INFO mapreduce.Job:  map 77% reduce 0%
18/05/18 05:15:13 INFO mapreduce.Job:  map 80% reduce 0%
18/05/18 05:15:16 INFO mapreduce.Job:  map 82% reduce 0%
18/05/18 05:15:17 INFO mapreduce.Job:  map 85% reduce 0%
18/05/18 05:15:18 INFO mapreduce.Job:  map 90% reduce 0%
18/05/18 05:15:23 INFO mapreduce.Job:  map 93% reduce 0%
18/05/18 05:15:24 INFO mapreduce.Job:  map 95% reduce 0%
18/05/18 05:15:25 INFO mapreduce.Job:  map 98% reduce 0%
18/05/18 05:15:26 INFO mapreduce.Job:  map 100% reduce 0%
18/05/18 05:15:26 INFO mapreduce.Job: Job job_1526617839979_0006 completed successfully
18/05/18 05:15:26 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=5107430
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=3423
		HDFS: Number of bytes written=5000000000
		HDFS: Number of read operations=160
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=80
	Job Counters
		Launched map tasks=40
		Other local map tasks=40
		Total time spent by all maps in occupied slots (ms)=276570
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=276570
		Total vcore-milliseconds taken by all map tasks=276570
		Total megabyte-milliseconds taken by all map tasks=283207680
	Map-Reduce Framework
		Map input records=50000000
		Map output records=50000000
		Input split bytes=3423
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=4007
		CPU time spent (ms)=177180
		Physical memory (bytes) snapshot=14019813376
		Virtual memory (bytes) snapshot=63008604160
		Total committed heap usage (bytes)=17951621120
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=107387891658806101
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=5000000000

real	1m17.340s
user	0m5.654s
sys	0m0.330s
[groot@ip-172-31-81-26 ~]$

```

## hdfs dfs -ls /user/groot/tgen
```
[groot@ip-172-31-81-26 ~]$ hdfs dfs -ls /user/groot/tgen
Found 41 items
-rw-r--r--   3 groot superuser          0 2018-05-18 05:15 /user/groot/tgen/_SUCCESS
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00000
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00001
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00002
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00003
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00004
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00005
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00006
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00007
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00008
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00009
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00010
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00011
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00012
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00013
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00014
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00015
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00016
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00017
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00018
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00019
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00020
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00021
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00022
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00023
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:14 /user/groot/tgen/part-m-00024
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00025
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00026
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00027
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00028
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00029
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00030
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00031
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00032
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00033
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00034
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00035
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00036
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00037
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00038
-rw-r--r--   3 groot superuser  125000000 2018-05-18 05:15 /user/groot/tgen/part-m-00039
[groot@ip-172-31-81-26 ~]$
```

## hadoop fsck -blocks /user/groot
```
[groot@ip-172-31-81-26 ~]$ hadoop fsck -blocks /user/groot
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Connecting to namenode via http://ip-172-31-92-45.ec2.internal:50070
FSCK started by groot (auth:SIMPLE) from /172.31.81.26 for path /user/groot at Fri May 18 05:20:37 UTC 2018
.........................................Status: HEALTHY
 Total size:	5000000000 B
 Total dirs:	3
 Total files:	41
 Total symlinks:		0
 Total blocks (validated):	80 (avg. block size 62500000 B)
 Minimally replicated blocks:	80 (100.0 %)
 Over-replicated blocks:	0 (0.0 %)
 Under-replicated blocks:	0 (0.0 %)
 Mis-replicated blocks:		0 (0.0 %)
 Default replication factor:	3
 Average block replication:	3.0
 Corrupt blocks:		0
 Missing replicas:		0 (0.0 %)
 Number of data-nodes:		3
 Number of racks:		1
FSCK ended at Fri May 18 05:20:37 UTC 2018 in 8 milliseconds


The filesystem under path '/user/groot' is HEALTHY
[groot@ip-172-31-81-26 ~]$
```
