
## HDFS Snapshot
<code>
[ferrarilin@ip-172-31-53-126 ~]$ sudo -u hdfs  hdfs dfsadmin -allowSnapshot /user/ferrarilin/precious/
Allowing snaphot on /user/ferrarilin/precious/ succeeded
[ferrarilin@ip-172-31-53-126 ~]$ hdfs dfs -createSnapshot /user/ferrarilin/precious sebc-hdfs-test
Created snapshot /user/ferrarilin/precious/.snapshot/sebc-hdfs-test
[ferrarilin@ip-172-31-53-126 ~]$ hdfs lsSnapshottableDir
drwxr-xr-x 0 ferrarilin supergroup 0 2018-05-16 07:40 1 65536 /user/ferrarilin/precious
[ferrarilin@ip-172-31-53-126 ~]$
</code>  
