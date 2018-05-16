## <center>1.Teragen 500MB Data </p>
<code>
[root@ip-172-31-55-193 home]# sudo -u hdfs time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples.jar teragen 5000000 /teragen
18/05/16 04:38:41 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-55-156.ec2.internal/172.31.55.156:8032
18/05/16 04:38:41 INFO terasort.TeraGen: Generating 5000000 using 2
18/05/16 04:38:42 INFO mapreduce.JobSubmitter: number of splits:2
18/05/16 04:38:42 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1526436876141_0002
18/05/16 04:38:42 INFO impl.YarnClientImpl: Submitted application application_1526436876141_0002
18/05/16 04:38:42 INFO mapreduce.Job: The url to track the job: http://ip-172-31-55-156.ec2.internal:8088/proxy/application_1526436876141_0002/
18/05/16 04:38:42 INFO mapreduce.Job: Running job: job_1526436876141_0002
18/05/16 04:38:48 INFO mapreduce.Job: Job job_1526436876141_0002 running in uber mode : false
18/05/16 04:38:48 INFO mapreduce.Job:  map 0% reduce 0%
18/05/16 04:38:57 INFO mapreduce.Job:  map 50% reduce 0%
18/05/16 04:38:58 INFO mapreduce.Job:  map 100% reduce 0%
18/05/16 04:38:58 INFO mapreduce.Job: Job job_1526436876141_0002 completed successfully
18/05/16 04:38:58 INFO mapreduce.Job: Counters: 31
	File System Counters
		FILE: Number of bytes read=0
		FILE: Number of bytes written=297876
		FILE: Number of read operations=0
		FILE: Number of large read operations=0
		FILE: Number of write operations=0
		HDFS: Number of bytes read=167
		HDFS: Number of bytes written=500000000
		HDFS: Number of read operations=8
		HDFS: Number of large read operations=0
		HDFS: Number of write operations=4
	Job Counters
		Launched map tasks=2
		Other local map tasks=2
		Total time spent by all maps in occupied slots (ms)=15965
		Total time spent by all reduces in occupied slots (ms)=0
		Total time spent by all map tasks (ms)=15965
		Total vcore-milliseconds taken by all map tasks=15965
		Total megabyte-milliseconds taken by all map tasks=16348160
	Map-Reduce Framework
		Map input records=5000000
		Map output records=5000000
		Input split bytes=167
		Spilled Records=0
		Failed Shuffles=0
		Merged Map outputs=0
		GC time elapsed (ms)=247
		CPU time spent (ms)=12570
		Physical memory (bytes) snapshot=763027456
		Virtual memory (bytes) snapshot=3130892288
		Total committed heap usage (bytes)=893911040
	org.apache.hadoop.examples.terasort.TeraGen$Counters
		CHECKSUM=10735710707299981
	File Input Format Counters
		Bytes Read=0
	File Output Format Counters
		Bytes Written=500000000
5.28user 0.31system 0:19.78elapsed 28%CPU (0avgtext+0avgdata 248928maxresident)k
0inputs+1816outputs (0major+84618minor)pagefaults 0swaps
[root@ip-172-31-55-193 home]#  
</code>


## <center>2.Use hdfs fsck path -files -blocks</p>
<code>
[root@ip-172-31-55-193 home]# hdfs fsck / -files -blocks
Connecting to namenode via http://ip-172-31-55-156.ec2.internal:50070/fsck?ugi=root&files=1&blocks=1&path=%2F
FSCK started by root (auth:SIMPLE) from /172.31.55.193 for path / at Wed May 16 04:44:05 UTC 2018
/ <dir>
/teragen <dir>
/teragen/_SUCCESS 0 bytes, 0 block(s):  OK

/teragen/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-241095163-172.31.55.156-1526436827479:blk_1073744379_3555 len=134217728 Live_repl=3
1. BP-241095163-172.31.55.156-1526436827479:blk_1073744381_3557 len=115782272 Live_repl=3

/teragen/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-241095163-172.31.55.156-1526436827479:blk_1073744380_3556 len=134217728 Live_repl=3
1. BP-241095163-172.31.55.156-1526436827479:blk_1073744382_3558 len=115782272 Live_repl=3

/tmp <dir>
/tmp/.cloudera_health_monitoring_canary_files <dir>
FSCK ended at Wed May 16 04:44:05 UTC 2018 in 2 milliseconds
Permission denied: user=root, access=READ_EXECUTE, inode="/tmp/.cloudera_health_monitoring_canary_files":hdfs:supergroup:d---------


Fsck on path '/' FAILED
[root@ip-172-31-55-193 home]#
</code>  
