## Pi
```
[root@ip-172-31-94-28 home]# sudo -u thanos hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar pi 2 4
Number of Maps  = 2
Samples per Map = 4
Wrote input for Map #0
Wrote input for Map #1
Starting Job
18/05/18 05:42:29 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-87-98.ec2.internal/172.31.87.98:8032
18/05/18 05:42:29 INFO input.FileInputFormat: Total input paths to process : 2
18/05/18 05:42:30 INFO mapreduce.JobSubmitter: number of splits:2
18/05/18 05:42:30 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526617839979_0008
18/05/18 05:42:30 INFO impl.YarnClientImpl: Submitted application application_1526617839979_0008
18/05/18 05:42:30 INFO mapreduce.Job: The url to track the job: http://ip-172-31-87-98.ec2.internal:8088/proxy/application_1526617839979_0008/
18/05/18 05:42:30 INFO mapreduce.Job: Running job: job_1526617839979_0008
18/05/18 05:42:40 INFO mapreduce.Job: Job job_1526617839979_0008 running in uber mode : false
18/05/18 05:42:40 INFO mapreduce.Job:  map 0% reduce 0%
18/05/18 05:42:47 INFO mapreduce.Job:  map 50% reduce 0%
18/05/18 05:42:52 INFO mapreduce.Job:  map 100% reduce 0%
18/05/18 05:43:03 INFO mapreduce.Job:  map 100% reduce 100%
18/05/18 05:43:03 INFO mapreduce.Job: Job job_1526617839979_0008 completed successfully
18/05/18 05:43:03 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=47
		FILE: Number of bytes written=385160
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=570
		HDFS: Number of bytes written=215
		HDFS: Number of read operations=11
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=3
	Job Counters
		Launched map tasks=2
		Launched reduce tasks=1
		Data-local map tasks=2
		Total time spent by all maps in occupied slots (ms)=7594
		Total time spent by all reduces in occupied slots (ms)=3526
		Total time spent by all map tasks (ms)=7594
		Total time spent by all reduce tasks (ms)=3526
		Total vcore-milliseconds taken by all map tasks=7594
		Total vcore-milliseconds taken by all reduce tasks=3526
		Total megabyte-milliseconds taken by all map tasks=7776256
		Total megabyte-milliseconds taken by all reduce tasks=3610624
	Map-Reduce Framework
		Map input records=2
		Map output records=4
		Map output bytes=36
		Map output materialized bytes=67
		Input split bytes=334
		Combine input records=0
		Combine output records=0
		Reduce input groups=2
		Reduce shuffle bytes=67
		Reduce input records=4
		Reduce output records=0
		Spilled Records=8
		Shuffled Maps =2
		Failed Shuffles=0
		Merged Map outputs=2
		GC time elapsed (ms)=89
		CPU time spent (ms)=2340
		Physical memory (bytes) snapshot=1165930496
		Virtual memory (bytes) snapshot=4743217152
		Total committed heap usage (bytes)=1424490496
	Shuffle Errors
		BAD_ID=0
		CONNECTION=0
		IO_ERROR=0
		WRONG_LENGTH=0
		WRONG_MAP=0
		WRONG_REDUCE=0
	File Input Format Counters
		Bytes Read=236
	File Output Format Counters
		Bytes Written=97
Job Finished in 34.217 seconds
Estimated value of Pi is 3.50000000000000000000
[root@ip-172-31-94-28 home]#
```
