## hostname
```
[root@ip-172-31-92-45 home]# hostname -f
ip-172-31-92-45.ec2.internal
[root@ip-172-31-92-45 home]#
```
## Status
```
[root@ip-172-31-92-45 home]# mysql -uscm -pscm -e "status;"
--------------
mysql  Ver 14.14 Distrib 5.5.60, for Linux (x86_64) using readline 5.1

Connection id:		11
Current database:
Current user:		scm@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		5.5.60 MySQL Community Server (GPL)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	latin1
Conn.  characterset:	latin1
UNIX socket:		/var/lib/mysql/mysql.sock
Uptime:			2 min 41 sec

Threads: 1  Questions: 46  Slow queries: 0  Opens: 34  Flush tables: 1  Open tables: 27  Queries per second avg: 0.285
--------------

[root@ip-172-31-92-45 home]# mysql -urman -prman -e "status;"
--------------
mysql  Ver 14.14 Distrib 5.5.60, for Linux (x86_64) using readline 5.1

Connection id:		12
Current database:
Current user:		rman@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		5.5.60 MySQL Community Server (GPL)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	latin1
Conn.  characterset:	latin1
UNIX socket:		/var/lib/mysql/mysql.sock
Uptime:			2 min 41 sec

Threads: 1  Questions: 51  Slow queries: 0  Opens: 34  Flush tables: 1  Open tables: 27  Queries per second avg: 0.316
--------------

[root@ip-172-31-92-45 home]# mysql -uhue -phue -e "status;"
--------------
mysql  Ver 14.14 Distrib 5.5.60, for Linux (x86_64) using readline 5.1

Connection id:		14
Current database:
Current user:		hue@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		5.5.60 MySQL Community Server (GPL)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	latin1
Conn.  characterset:	latin1
UNIX socket:		/var/lib/mysql/mysql.sock
Uptime:			2 min 41 sec

Threads: 1  Questions: 56  Slow queries: 0  Opens: 34  Flush tables: 1  Open tables: 27  Queries per second avg: 0.347
--------------

[root@ip-172-31-92-45 home]# mysql -usentry -psentry -e "status;"
--------------
mysql  Ver 14.14 Distrib 5.5.60, for Linux (x86_64) using readline 5.1

Connection id:		15
Current database:
Current user:		sentry@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		5.5.60 MySQL Community Server (GPL)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	latin1
Conn.  characterset:	latin1
UNIX socket:		/var/lib/mysql/mysql.sock
Uptime:			2 min 41 sec

Threads: 1  Questions: 61  Slow queries: 0  Opens: 34  Flush tables: 1  Open tables: 27  Queries per second avg: 0.378
--------------

[root@ip-172-31-92-45 home]# mysql -uoozie -poozie -e "status;"
--------------
mysql  Ver 14.14 Distrib 5.5.60, for Linux (x86_64) using readline 5.1

Connection id:		16
Current database:
Current user:		oozie@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		5.5.60 MySQL Community Server (GPL)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	latin1
Conn.  characterset:	latin1
UNIX socket:		/var/lib/mysql/mysql.sock
Uptime:			2 min 44 sec

Threads: 1  Questions: 66  Slow queries: 0  Opens: 34  Flush tables: 1  Open tables: 27  Queries per second avg: 0.402
--------------

[root@ip-172-31-92-45 home]# mysql -umetastore -phive -e "status;"
--------------
mysql  Ver 14.14 Distrib 5.5.60, for Linux (x86_64) using readline 5.1

Connection id:		56
Current database:
Current user:		metastore@localhost
SSL:			Not in use
Current pager:		stdout
Using outfile:		''
Using delimiter:	;
Server version:		5.5.60 MySQL Community Server (GPL)
Protocol version:	10
Connection:		Localhost via UNIX socket
Server characterset:	latin1
Db     characterset:	latin1
Client characterset:	latin1
Conn.  characterset:	latin1
UNIX socket:		/var/lib/mysql/mysql.sock
Uptime:			17 min 14 sec

Threads: 1  Questions: 175  Slow queries: 0  Opens: 34  Flush tables: 1  Open tables: 27  Queries per second avg: 0.169
--------------

[root@ip-172-31-92-45 home]#

```
## show Database 
```
[root@ip-172-31-92-45 home]# mysql -uscm -pscm -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| scm                |
+--------------------+
[root@ip-172-31-92-45 home]# mysql -urman -prman -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| rman               |
+--------------------+
[root@ip-172-31-92-45 home]# mysql -uhue -phue -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hue                |
+--------------------+
[root@ip-172-31-92-45 home]# mysql -usentry -psentry -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| sentry             |
+--------------------+
[root@ip-172-31-92-45 home]# mysql -uoozie -poozie -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| oozie              |
+--------------------+
[root@ip-172-31-92-45 home]# mysql -umetastore -phive -e "show databases;"
+--------------------+
| Database           |
+--------------------+
| information_schema |
| metastore          |
+--------------------+
[root@ip-172-31-92-45 home]#

```
