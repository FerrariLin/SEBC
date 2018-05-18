## Terasort
```
[groot@ip-172-31-81-26 ~]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/groot/tgen /user/groot/tsort
18/05/18 05:40:35 INFO terasort.TeraSort: starting
18/05/18 05:40:37 INFO input.FileInputFormat: Total input paths to process : 40
Spent 195ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 200ms
Sampling 10 splits of 80
Making 6 from 100000 sampled records
Computing parititions took 873ms
Spent 1075ms computing partitions.
18/05/18 05:40:38 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-87-98.ec2.internal/172.31.87.98:8032
18/05/18 05:40:38 INFO mapreduce.JobSubmitter: number of splits:80
18/05/18 05:40:38 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526617839979_0007
18/05/18 05:40:39 INFO impl.YarnClientImpl: Submitted application application_1526617839979_0007
18/05/18 05:40:39 INFO mapreduce.Job: The url to track the job: http://ip-172-31-87-98.ec2.internal:8088/proxy/application_1526617839979_0007/
18/05/18 05:40:39 INFO mapreduce.Job: Running job: job_1526617839979_0007
18/05/18 05:40:45 INFO mapreduce.Job: Job job_1526617839979_0007 running in uber mode : false
18/05/18 05:40:45 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 05:40:54 INFO mapreduce.Job:  map 1% reduce 0%
18/05/18 05:40:56 INFO mapreduce.Job:  map 6% reduce 0%
18/05/18 05:41:00 INFO mapreduce.Job:  map 8% reduce 0%
18/05/18 05:41:04 INFO mapreduce.Job:  map 13% reduce 0%
18/05/18 05:41:07 INFO mapreduce.Job:  map 14% reduce 0%
18/05/18 05:41:12 INFO mapreduce.Job:  map 17% reduce 0%
18/05/18 05:41:13 INFO mapreduce.Job:  map 19% reduce 0%
18/05/18 05:41:14 INFO mapreduce.Job:  map 20% reduce 0%
18/05/18 05:41:20 INFO mapreduce.Job:  map 25% reduce 0%
18/05/18 05:41:21 INFO mapreduce.Job:  map 26% reduce 0%
18/05/18 05:41:27 INFO mapreduce.Job:  map 28% reduce 0%
18/05/18 05:41:28 INFO mapreduce.Job:  map 30% reduce 0%
18/05/18 05:41:29 INFO mapreduce.Job:  map 31% reduce 0%
18/05/18 05:41:30 INFO mapreduce.Job:  map 32% reduce 0%
18/05/18 05:41:34 INFO mapreduce.Job:  map 34% reduce 0%
18/05/18 05:41:36 INFO mapreduce.Job:  map 36% reduce 0%
18/05/18 05:41:37 INFO mapreduce.Job:  map 38% reduce 0%
18/05/18 05:41:38 INFO mapreduce.Job:  map 39% reduce 0%
18/05/18 05:41:40 INFO mapreduce.Job:  map 40% reduce 0%
18/05/18 05:41:44 INFO mapreduce.Job:  map 43% reduce 0%
18/05/18 05:41:45 INFO mapreduce.Job:  map 44% reduce 0%
18/05/18 05:41:46 INFO mapreduce.Job:  map 45% reduce 0%
18/05/18 05:41:47 INFO mapreduce.Job:  map 46% reduce 0%
18/05/18 05:41:52 INFO mapreduce.Job:  map 49% reduce 0%
18/05/18 05:41:53 INFO mapreduce.Job:  map 50% reduce 0%
18/05/18 05:41:54 INFO mapreduce.Job:  map 52% reduce 0%
18/05/18 05:42:00 INFO mapreduce.Job:  map 56% reduce 0%
18/05/18 05:42:01 INFO mapreduce.Job:  map 57% reduce 0%
18/05/18 05:42:02 INFO mapreduce.Job:  map 59% reduce 0%
18/05/18 05:42:06 INFO mapreduce.Job:  map 60% reduce 0%
18/05/18 05:42:08 INFO mapreduce.Job:  map 63% reduce 0%
18/05/18 05:42:09 INFO mapreduce.Job:  map 64% reduce 0%
18/05/18 05:42:10 INFO mapreduce.Job:  map 65% reduce 0%
18/05/18 05:42:12 INFO mapreduce.Job:  map 66% reduce 0%
18/05/18 05:42:16 INFO mapreduce.Job:  map 69% reduce 0%
18/05/18 05:42:17 INFO mapreduce.Job:  map 70% reduce 0%
18/05/18 05:42:18 INFO mapreduce.Job:  map 73% reduce 0%
18/05/18 05:42:24 INFO mapreduce.Job:  map 76% reduce 0%
18/05/18 05:42:25 INFO mapreduce.Job:  map 77% reduce 0%
18/05/18 05:42:26 INFO mapreduce.Job:  map 79% reduce 0%
18/05/18 05:42:31 INFO mapreduce.Job:  map 80% reduce 0%
18/05/18 05:42:32 INFO mapreduce.Job:  map 81% reduce 0%
18/05/18 05:42:33 INFO mapreduce.Job:  map 82% reduce 0%
18/05/18 05:42:34 INFO mapreduce.Job:  map 85% reduce 0%
18/05/18 05:42:37 INFO mapreduce.Job:  map 86% reduce 0%
18/05/18 05:42:40 INFO mapreduce.Job:  map 88% reduce 0%
18/05/18 05:42:41 INFO mapreduce.Job:  map 89% reduce 0%
18/05/18 05:42:48 INFO mapreduce.Job:  map 90% reduce 0%
18/05/18 05:42:52 INFO mapreduce.Job:  map 90% reduce 5%
18/05/18 05:42:53 INFO mapreduce.Job:  map 90% reduce 10%
18/05/18 05:42:54 INFO mapreduce.Job:  map 91% reduce 10%
18/05/18 05:42:58 INFO mapreduce.Job:  map 93% reduce 10%
18/05/18 05:43:01 INFO mapreduce.Job:  map 94% reduce 10%
18/05/18 05:43:08 INFO mapreduce.Job:  map 95% reduce 10%
18/05/18 05:43:09 INFO mapreduce.Job:  map 96% reduce 10%
18/05/18 05:43:11 INFO mapreduce.Job:  map 96% reduce 11%
18/05/18 05:43:16 INFO mapreduce.Job:  map 98% reduce 11%
18/05/18 05:43:17 INFO mapreduce.Job:  map 99% reduce 11%
18/05/18 05:43:18 INFO mapreduce.Job:  map 100% reduce 11%
18/05/18 05:43:22 INFO mapreduce.Job:  map 100% reduce 17%
18/05/18 05:43:23 INFO mapreduce.Job:  map 100% reduce 25%
18/05/18 05:43:28 INFO mapreduce.Job:  map 100% reduce 31%
18/05/18 05:43:32 INFO mapreduce.Job:  map 100% reduce 33%
18/05/18 05:43:33 INFO mapreduce.Job:  map 100% reduce 58%
18/05/18 05:43:35 INFO mapreduce.Job:  map 100% reduce 70%
18/05/18 05:43:39 INFO mapreduce.Job:  map 100% reduce 77%
18/05/18 05:43:41 INFO mapreduce.Job:  map 100% reduce 80%
18/05/18 05:43:42 INFO mapreduce.Job:  map 100% reduce 82%
18/05/18 05:43:43 INFO mapreduce.Job:  map 100% reduce 95%
18/05/18 05:43:44 INFO mapreduce.Job:  map 100% reduce 97%
18/05/18 05:43:48 INFO mapreduce.Job:  map 100% reduce 100%
18/05/18 05:43:48 INFO mapreduce.Job: Job job_1526617839979_0007 completed successfully
18/05/18 05:43:48 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=2241599712
		FILE: Number of bytes written=4444036360
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=5000010720
		HDFS: Number of bytes written=5000000000
		HDFS: Number of read operations=258
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters
		Launched map tasks=80
		Launched reduce tasks=6
		Data-local map tasks=80
		Total time spent by all maps in occupied slots (ms)=535431
		Total time spent by all reduces in occupied slots (ms)=196581
		Total time spent by all map tasks (ms)=535431
		Total time spent by all reduce tasks (ms)=196581
		Total vcore-milliseconds taken by all map tasks=535431
		Total vcore-milliseconds taken by all reduce tasks=196581
		Total megabyte-milliseconds taken by all map tasks=548281344
		Total megabyte-milliseconds taken by all reduce tasks=201298944
	Map-Reduce Framework
		Map input records=50000000
		Map output records=50000000
		Map output bytes=5100000000
		Map output materialized bytes=2191331086
		Input split bytes=10720
		Combine input records=0
		Combine output records=0
		Reduce input groups=50000000
		Reduce shuffle bytes=2191331086
		Reduce input records=50000000
		Reduce output records=50000000
		Spilled Records=100000000
		Shuffled Maps =480
		Failed Shuffles=0
		Merged Map outputs=480
		GC time elapsed (ms)=10549
		CPU time spent (ms)=497930
		Physical memory (bytes) snapshot=46993100800
		Virtual memory (bytes) snapshot=135517888512
		Total committed heap usage (bytes)=54786523136
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=5000000000
	File Output Format Counters
		Bytes Written=5000000000
18/05/18 05:43:48 INFO terasort.TeraSort: done
[groot@ip-172-31-81-26 ~]$
```
