# Cloudera-scm-Server Log
```
[root@ip-172-31-87-98 html]# head -1 /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-05-18 03:58:27,346 INFO main:com.cloudera.server.cmf.Main: Starting SCM Server. JVM Args: [-Dlog4j.configuration=file:/etc/cloudera-scm-server/log4j.properties, -Dfile.encoding=UTF-8, -Dcmf.root.logger=INFO,LOGFILE, -Dcmf.log.dir=/var/log/cloudera-scm-server, -Dcmf.log.file=cloudera-scm-server.log, -Dcmf.jetty.threshhold=WARN, -Dcmf.schema.dir=/usr/share/cmf/schema, -Djava.awt.headless=true, -Djava.net.preferIPv4Stack=true, -Dpython.home=/usr/share/cmf/python, -XX:+UseConcMarkSweepGC, -XX:+UseParNewGC, -XX:+HeapDumpOnOutOfMemoryError, -Xmx2G, -XX:MaxPermSize=256m, -XX:+HeapDumpOnOutOfMemoryError, -XX:HeapDumpPath=/tmp, -XX:OnOutOfMemoryError=kill -9 %p], Args: [], Version: 5.11.2 (#6 built by jenkins on 20170811-0014 git: 3c3ea33a12076fb83a8f11c4452c52fac685d01b)
[root@ip-172-31-87-98 html]#
```
## END Log
```
[root@ip-172-31-87-98 html]# tailf  /var/log/cloudera-scm-server/cloudera-scm-server.log
2018-05-18 03:59:35,438 INFO SearchRepositoryManager-0:com.cloudera.server.web.cmf.search.components.SearchRepositoryManager: Generating documents:2018-05-18T03:59:35.438Z
2018-05-18 03:59:35,461 INFO SearchRepositoryManager-0:com.cloudera.server.web.cmf.search.components.SearchRepositoryManager: Num docs:207
2018-05-18 03:59:35,462 INFO SearchRepositoryManager-0:com.cloudera.server.web.cmf.search.components.SearchRepositoryManager: Constructing repo:2018-05-18T03:59:35.462Z
2018-05-18 03:59:35,581 INFO WebServerImpl:com.cloudera.server.web.cmf.AggregatorController: AggregateSummaryScheduler started.
2018-05-18 03:59:36,365 INFO SearchRepositoryManager-0:com.cloudera.server.web.cmf.search.components.SearchRepositoryManager: Finished constructing repo:2018-05-18T03:59:36.365Z
2018-05-18 03:59:36,936 INFO WebServerImpl:org.mortbay.log: jetty-6.1.26.cloudera.4
2018-05-18 03:59:36,937 INFO WebServerImpl:org.mortbay.log: Started SelectChannelConnector@0.0.0.0:7180
2018-05-18 03:59:36,937 INFO WebServerImpl:com.cloudera.server.cmf.WebServerImpl: Started Jetty server.
2018-05-18 04:00:00,017 INFO com.cloudera.cmf.scheduler-1_Worker-1:com.cloudera.cmf.service.ServiceHandlerRegistry: Executing command GlobalPoolsRefresh BasicCmdArgs{scheduleId=1, scheduledTime=2018-05-18T04:00:00.000Z}.
2018-05-18 04:00:00,020 INFO com.cloudera.cmf.scheduler-1_Worker-1:com.cloudera.cmf.scheduler.CommandDispatcherJob: Skipping scheduled command 'GlobalPoolsRefresh' since it is a noop.
```
