## <center>teragen</p>
<code>
[ferrarilin@ip-172-31-55-193 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen -D dfs.block.size=33554432 100000000 /user/ferrarilin/teragen
18/05/16 06:48:36 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-55-156.ec2.internal/172.31.55.156:8032
18/05/16 06:48:37 INFO terasort.TeraGen: Generating 100000000 using 2
18/05/16 06:48:37 INFO mapreduce.JobSubmitter: number of splits:2
18/05/16 06:48:38 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
18/05/16 06:48:38 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526436876141_0125
18/05/16 06:48:38 INFO impl.YarnClientImpl: Submitted application application_1526436876141_0125
18/05/16 06:48:39 INFO mapreduce.Job: The url to track the job: http://ip-172-31-55-156.ec2.internal:8088/proxy/application_1526436876141_0125/
18/05/16 06:48:39 INFO mapreduce.Job: Running job: job_1526436876141_0125
18/05/16 06:48:51 INFO mapreduce.Job: Job job_1526436876141_0125 running in uber mode : false
18/05/16 06:48:51 INFO mapreduce.Job:  map 0% reduce 0%
18/05/16 06:49:14 INFO mapreduce.Job:  map 8% reduce 0%
18/05/16 06:49:20 INFO mapreduce.Job:  map 12% reduce 0%
18/05/16 06:49:26 INFO mapreduce.Job:  map 17% reduce 0%
18/05/16 06:49:32 INFO mapreduce.Job:  map 22% reduce 0%
18/05/16 06:49:38 INFO mapreduce.Job:  map 26% reduce 0%
18/05/16 06:49:44 INFO mapreduce.Job:  map 31% reduce 0%
18/05/16 06:49:50 INFO mapreduce.Job:  map 36% reduce 0%
18/05/16 06:49:56 INFO mapreduce.Job:  map 40% reduce 0%
18/05/16 06:50:02 INFO mapreduce.Job:  map 44% reduce 0%
18/05/16 06:50:08 INFO mapreduce.Job:  map 49% reduce 0%
18/05/16 06:50:15 INFO mapreduce.Job:  map 53% reduce 0%
18/05/16 06:50:21 INFO mapreduce.Job:  map 58% reduce 0%
18/05/16 06:50:27 INFO mapreduce.Job:  map 62% reduce 0%
18/05/16 06:50:33 INFO mapreduce.Job:  map 67% reduce 0%
18/05/16 06:50:39 INFO mapreduce.Job:  map 72% reduce 0%
18/05/16 06:50:45 INFO mapreduce.Job:  map 77% reduce 0%
18/05/16 06:50:51 INFO mapreduce.Job:  map 81% reduce 0%
18/05/16 06:50:57 INFO mapreduce.Job:  map 86% reduce 0%
18/05/16 06:51:03 INFO mapreduce.Job:  map 90% reduce 0%
18/05/16 06:51:09 INFO mapreduce.Job:  map 95% reduce 0%
18/05/16 06:51:14 INFO mapreduce.Job:  map 97% reduce 0%
18/05/16 06:51:15 INFO mapreduce.Job:  map 99% reduce 0%
18/05/16 06:51:16 INFO mapreduce.Job:  map 100% reduce 0%
18/05/16 06:51:16 INFO mapreduce.Job: Job job_1526436876141_0125 completed successfully
18/05/16 06:51:16 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=297982
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=170
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=283080
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=283080
		Total vcore-milliseconds taken by all map tasks=283080
		Total megabyte-milliseconds taken by all map tasks=289873920
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Input split bytes=170
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=2042
		CPU time spent (ms)=169010
		Physical memory (bytes) snapshot=500576256
		Virtual memory (bytes) snapshot=3131662336
		Total committed heap usage (bytes)=508559360
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=214760662691937609
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=10000000000

real	2m45.612s
user	0m7.553s
sys	0m0.431s
[ferrarilin@ip-172-31-55-193 ~]$
</code>
## <center>terasort</p>
<code>
[ferrarilin@ip-172-31-55-193 ~]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar terasort /user/ferrarilin/teragen /user/ferrarilin/terasort
18/05/16 06:53:30 INFO terasort.TeraSort: starting
18/05/16 06:53:33 INFO input.FileInputFormat: Total input paths to process : 2
Spent 324ms computing base-splits.
Spent 7ms computing TeraScheduler splits.
Computing input splits took 332ms
Sampling 10 splits of 298
Making 6 from 100000 sampled records
Computing parititions took 1652ms
Spent 1987ms computing partitions.
18/05/16 06:53:35 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-55-156.ec2.internal/172.31.55.156:8032
18/05/16 06:53:36 INFO mapreduce.JobSubmitter: number of splits:298
18/05/16 06:53:36 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526436876141_0131
18/05/16 06:53:37 INFO impl.YarnClientImpl: Submitted application application_1526436876141_0131
18/05/16 06:53:37 INFO mapreduce.Job: The url to track the job: http://ip-172-31-55-156.ec2.internal:8088/proxy/application_1526436876141_0131/
18/05/16 06:53:37 INFO mapreduce.Job: Running job: job_1526436876141_0131
18/05/16 06:53:47 INFO mapreduce.Job: Job job_1526436876141_0131 running in uber mode : false
18/05/16 06:53:47 INFO mapreduce.Job:  map 0% reduce 0%
18/05/16 06:54:06 INFO mapreduce.Job:  map 1% reduce 0%
18/05/16 06:54:07 INFO mapreduce.Job:  map 2% reduce 0%
18/05/16 06:54:08 INFO mapreduce.Job:  map 4% reduce 0%
18/05/16 06:54:22 INFO mapreduce.Job:  map 5% reduce 0%
18/05/16 06:54:25 INFO mapreduce.Job:  map 6% reduce 0%
18/05/16 06:54:26 INFO mapreduce.Job:  map 7% reduce 0%
18/05/16 06:54:36 INFO mapreduce.Job:  map 8% reduce 0%
18/05/16 06:54:42 INFO mapreduce.Job:  map 9% reduce 0%
18/05/16 06:54:43 INFO mapreduce.Job:  map 10% reduce 0%
18/05/16 06:54:45 INFO mapreduce.Job:  map 11% reduce 0%
18/05/16 06:54:53 INFO mapreduce.Job:  map 12% reduce 0%
18/05/16 06:55:00 INFO mapreduce.Job:  map 13% reduce 0%
18/05/16 06:55:02 INFO mapreduce.Job:  map 14% reduce 0%
18/05/16 06:55:03 INFO mapreduce.Job:  map 15% reduce 0%
18/05/16 06:55:11 INFO mapreduce.Job:  map 16% reduce 0%
18/05/16 06:55:19 INFO mapreduce.Job:  map 17% reduce 0%
18/05/16 06:55:20 INFO mapreduce.Job:  map 18% reduce 0%
18/05/16 06:55:24 INFO mapreduce.Job:  map 19% reduce 0%
18/05/16 06:55:34 INFO mapreduce.Job:  map 20% reduce 0%
18/05/16 06:55:37 INFO mapreduce.Job:  map 21% reduce 0%
18/05/16 06:55:39 INFO mapreduce.Job:  map 22% reduce 0%
18/05/16 06:55:42 INFO mapreduce.Job:  map 23% reduce 0%
18/05/16 06:55:54 INFO mapreduce.Job:  map 24% reduce 0%
18/05/16 06:55:55 INFO mapreduce.Job:  map 25% reduce 0%
18/05/16 06:55:56 INFO mapreduce.Job:  map 26% reduce 0%
18/05/16 06:55:58 INFO mapreduce.Job:  map 27% reduce 0%
18/05/16 06:56:11 INFO mapreduce.Job:  map 28% reduce 0%
18/05/16 06:56:13 INFO mapreduce.Job:  map 29% reduce 0%
18/05/16 06:56:14 INFO mapreduce.Job:  map 30% reduce 0%
18/05/16 06:56:17 INFO mapreduce.Job:  map 31% reduce 0%
18/05/16 06:56:28 INFO mapreduce.Job:  map 32% reduce 0%
18/05/16 06:56:32 INFO mapreduce.Job:  map 33% reduce 0%
18/05/16 06:56:33 INFO mapreduce.Job:  map 34% reduce 0%
18/05/16 06:56:42 INFO mapreduce.Job:  map 35% reduce 0%
18/05/16 06:56:48 INFO mapreduce.Job:  map 36% reduce 0%
18/05/16 06:56:50 INFO mapreduce.Job:  map 37% reduce 0%
18/05/16 06:56:52 INFO mapreduce.Job:  map 38% reduce 0%
18/05/16 06:57:00 INFO mapreduce.Job:  map 39% reduce 0%
18/05/16 06:57:06 INFO mapreduce.Job:  map 40% reduce 0%
18/05/16 06:57:09 INFO mapreduce.Job:  map 41% reduce 0%
18/05/16 06:57:10 INFO mapreduce.Job:  map 42% reduce 0%
18/05/16 06:57:20 INFO mapreduce.Job:  map 43% reduce 0%
18/05/16 06:57:25 INFO mapreduce.Job:  map 44% reduce 0%
18/05/16 06:57:27 INFO mapreduce.Job:  map 45% reduce 0%
18/05/16 06:57:29 INFO mapreduce.Job:  map 46% reduce 0%
18/05/16 06:57:38 INFO mapreduce.Job:  map 47% reduce 0%
18/05/16 06:57:44 INFO mapreduce.Job:  map 48% reduce 0%
18/05/16 06:57:45 INFO mapreduce.Job:  map 49% reduce 0%
18/05/16 06:57:47 INFO mapreduce.Job:  map 50% reduce 0%
18/05/16 06:58:00 INFO mapreduce.Job:  map 51% reduce 0%
18/05/16 06:58:02 INFO mapreduce.Job:  map 52% reduce 0%
18/05/16 06:58:03 INFO mapreduce.Job:  map 53% reduce 0%
18/05/16 06:58:11 INFO mapreduce.Job:  map 54% reduce 0%
18/05/16 06:58:19 INFO mapreduce.Job:  map 55% reduce 0%
18/05/16 06:58:21 INFO mapreduce.Job:  map 57% reduce 0%
18/05/16 06:58:31 INFO mapreduce.Job:  map 58% reduce 0%
18/05/16 06:58:36 INFO mapreduce.Job:  map 59% reduce 0%
18/05/16 06:58:39 INFO mapreduce.Job:  map 60% reduce 0%
18/05/16 06:58:40 INFO mapreduce.Job:  map 61% reduce 0%
18/05/16 06:58:50 INFO mapreduce.Job:  map 62% reduce 0%
18/05/16 06:58:55 INFO mapreduce.Job:  map 63% reduce 0%
18/05/16 06:58:57 INFO mapreduce.Job:  map 64% reduce 0%
18/05/16 06:58:58 INFO mapreduce.Job:  map 65% reduce 0%
18/05/16 06:59:08 INFO mapreduce.Job:  map 66% reduce 0%
18/05/16 06:59:14 INFO mapreduce.Job:  map 67% reduce 0%
18/05/16 06:59:15 INFO mapreduce.Job:  map 68% reduce 0%
18/05/16 06:59:22 INFO mapreduce.Job:  map 69% reduce 0%
18/05/16 06:59:26 INFO mapreduce.Job:  map 70% reduce 0%
18/05/16 06:59:32 INFO mapreduce.Job:  map 71% reduce 0%
18/05/16 06:59:34 INFO mapreduce.Job:  map 72% reduce 0%
18/05/16 06:59:40 INFO mapreduce.Job:  map 73% reduce 0%
18/05/16 06:59:49 INFO mapreduce.Job:  map 74% reduce 0%
18/05/16 06:59:52 INFO mapreduce.Job:  map 76% reduce 0%
18/05/16 06:59:58 INFO mapreduce.Job:  map 77% reduce 0%
18/05/16 07:00:07 INFO mapreduce.Job:  map 78% reduce 0%
18/05/16 07:00:10 INFO mapreduce.Job:  map 79% reduce 0%
18/05/16 07:00:12 INFO mapreduce.Job:  map 80% reduce 0%
18/05/16 07:00:15 INFO mapreduce.Job:  map 81% reduce 0%
18/05/16 07:00:27 INFO mapreduce.Job:  map 82% reduce 0%
18/05/16 07:00:30 INFO mapreduce.Job:  map 83% reduce 0%
18/05/16 07:00:31 INFO mapreduce.Job:  map 84% reduce 0%
18/05/16 07:00:36 INFO mapreduce.Job:  map 85% reduce 0%
18/05/16 07:00:48 INFO mapreduce.Job:  map 86% reduce 0%
18/05/16 07:00:51 INFO mapreduce.Job:  map 86% reduce 3%
18/05/16 07:00:52 INFO mapreduce.Job:  map 86% reduce 5%
18/05/16 07:00:53 INFO mapreduce.Job:  map 86% reduce 9%
18/05/16 07:00:54 INFO mapreduce.Job:  map 87% reduce 9%
18/05/16 07:00:57 INFO mapreduce.Job:  map 87% reduce 11%
18/05/16 07:00:58 INFO mapreduce.Job:  map 87% reduce 12%
18/05/16 07:00:59 INFO mapreduce.Job:  map 87% reduce 14%
18/05/16 07:01:03 INFO mapreduce.Job:  map 87% reduce 15%
18/05/16 07:01:04 INFO mapreduce.Job:  map 88% reduce 15%
18/05/16 07:01:09 INFO mapreduce.Job:  map 88% reduce 17%
18/05/16 07:01:10 INFO mapreduce.Job:  map 88% reduce 18%
18/05/16 07:01:11 INFO mapreduce.Job:  map 89% reduce 20%
18/05/16 07:01:15 INFO mapreduce.Job:  map 89% reduce 21%
18/05/16 07:01:20 INFO mapreduce.Job:  map 90% reduce 21%
18/05/16 07:01:21 INFO mapreduce.Job:  map 90% reduce 22%
18/05/16 07:01:22 INFO mapreduce.Job:  map 90% reduce 23%
18/05/16 07:01:23 INFO mapreduce.Job:  map 90% reduce 25%
18/05/16 07:01:28 INFO mapreduce.Job:  map 91% reduce 25%
18/05/16 07:01:37 INFO mapreduce.Job:  map 92% reduce 25%
18/05/16 07:01:43 INFO mapreduce.Job:  map 93% reduce 25%
18/05/16 07:01:45 INFO mapreduce.Job:  map 93% reduce 26%
18/05/16 07:01:52 INFO mapreduce.Job:  map 94% reduce 26%
18/05/16 07:01:55 INFO mapreduce.Job:  map 95% reduce 26%
18/05/16 07:02:05 INFO mapreduce.Job:  map 96% reduce 26%
18/05/16 07:02:09 INFO mapreduce.Job:  map 96% reduce 27%
18/05/16 07:02:12 INFO mapreduce.Job:  map 97% reduce 27%
18/05/16 07:02:21 INFO mapreduce.Job:  map 98% reduce 27%
18/05/16 07:02:25 INFO mapreduce.Job:  map 99% reduce 27%
18/05/16 07:02:34 INFO mapreduce.Job:  map 99% reduce 28%
18/05/16 07:02:35 INFO mapreduce.Job:  map 100% reduce 28%
18/05/16 07:02:39 INFO mapreduce.Job:  map 100% reduce 33%
18/05/16 07:02:40 INFO mapreduce.Job:  map 100% reduce 38%
18/05/16 07:02:41 INFO mapreduce.Job:  map 100% reduce 47%
18/05/16 07:02:45 INFO mapreduce.Job:  map 100% reduce 53%
18/05/16 07:02:46 INFO mapreduce.Job:  map 100% reduce 56%
18/05/16 07:02:47 INFO mapreduce.Job:  map 100% reduce 58%
18/05/16 07:02:51 INFO mapreduce.Job:  map 100% reduce 59%
18/05/16 07:02:52 INFO mapreduce.Job:  map 100% reduce 61%
18/05/16 07:02:53 INFO mapreduce.Job:  map 100% reduce 62%
18/05/16 07:02:57 INFO mapreduce.Job:  map 100% reduce 63%
18/05/16 07:02:58 INFO mapreduce.Job:  map 100% reduce 64%
18/05/16 07:02:59 INFO mapreduce.Job:  map 100% reduce 65%
18/05/16 07:03:04 INFO mapreduce.Job:  map 100% reduce 66%
18/05/16 07:03:05 INFO mapreduce.Job:  map 100% reduce 68%
18/05/16 07:03:06 INFO mapreduce.Job:  map 100% reduce 69%
18/05/16 07:03:10 INFO mapreduce.Job:  map 100% reduce 70%
18/05/16 07:03:11 INFO mapreduce.Job:  map 100% reduce 71%
18/05/16 07:03:12 INFO mapreduce.Job:  map 100% reduce 73%
18/05/16 07:03:17 INFO mapreduce.Job:  map 100% reduce 76%
18/05/16 07:03:18 INFO mapreduce.Job:  map 100% reduce 77%
18/05/16 07:03:23 INFO mapreduce.Job:  map 100% reduce 79%
18/05/16 07:03:24 INFO mapreduce.Job:  map 100% reduce 80%
18/05/16 07:03:27 INFO mapreduce.Job:  map 100% reduce 81%
18/05/16 07:03:29 INFO mapreduce.Job:  map 100% reduce 86%
18/05/16 07:03:31 INFO mapreduce.Job:  map 100% reduce 87%
18/05/16 07:03:35 INFO mapreduce.Job:  map 100% reduce 90%
18/05/16 07:03:37 INFO mapreduce.Job:  map 100% reduce 91%
18/05/16 07:03:41 INFO mapreduce.Job:  map 100% reduce 92%
18/05/16 07:03:43 INFO mapreduce.Job:  map 100% reduce 93%
18/05/16 07:03:47 INFO mapreduce.Job:  map 100% reduce 94%
18/05/16 07:03:49 INFO mapreduce.Job:  map 100% reduce 95%
18/05/16 07:03:53 INFO mapreduce.Job:  map 100% reduce 96%
18/05/16 07:03:59 INFO mapreduce.Job:  map 100% reduce 97%
18/05/16 07:04:05 INFO mapreduce.Job:  map 100% reduce 98%
18/05/16 07:04:11 INFO mapreduce.Job:  map 100% reduce 99%
18/05/16 07:04:17 INFO mapreduce.Job:  map 100% reduce 100%
18/05/16 07:04:20 INFO mapreduce.Job: Job job_1526436876141_0131 completed successfully
18/05/16 07:04:20 INFO mapreduce.Job: Counters: 49
	File System Counters
		FILE: Number of bytes read=4477356344
		FILE: Number of bytes written=8898094666
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=10000042614
		HDFS: Number of bytes written=10000000000
		HDFS: Number of read operations=912
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=12
	Job Counters
		Launched map tasks=298
		Launched reduce tasks=6
		Data-local map tasks=298
		Total time spent by all maps in occupied slots (ms)=4735908
		Total time spent by all reduces in occupied slots (ms)=1070589
		Total time spent by all map tasks (ms)=4735908
		Total time spent by all reduce tasks (ms)=1070589
		Total vcore-milliseconds taken by all map tasks=4735908
		Total vcore-milliseconds taken by all reduce tasks=1070589
		Total megabyte-milliseconds taken by all map tasks=4849569792
		Total megabyte-milliseconds taken by all reduce tasks=1096283136
	Map-Reduce Framework
		Map input records=100000000
		Map output records=100000000
		Map output bytes=10200000000
		Map output materialized bytes=4374945516
		Input split bytes=42614
		Combine input records=0
		Combine output records=0
		Reduce input groups=100000000
		Reduce shuffle bytes=4374945516
		Reduce input records=100000000
		Reduce output records=100000000
		Spilled Records=200000000
		Shuffled Maps =1788
		Failed Shuffles=0
		Merged Map outputs=1788
		GC time elapsed (ms)=55257
		CPU time spent (ms)=1489630
		Physical memory (bytes) snapshot=146117881856
		Virtual memory (bytes) snapshot=477691195392
		Total committed heap usage (bytes)=173105217536
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
18/05/16 07:04:20 INFO terasort.TeraSort: done

real	10m52.555s
user	0m11.966s
sys	0m0.704s
[ferrarilin@ip-172-31-55-193 ~]$
</code>



