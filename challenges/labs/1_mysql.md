1_mysql.md

Mysql Hostname: ip-172-31-25-177

Mysql Version

	[root@ip-172-31-25-177 yum.repos.d]# mysql --version
	mysql  Ver 14.14 Distrib 5.5.54, for Linux (x86_64) using readline 5.1

Mysql Databases

	mysql> show databases;
	+--------------------+
	| Database           |
	+--------------------+
	| information_schema |
	| hive               |
	| mysql              |
	| oozie              |
	| performance_schema |
	| rman               |
	| scm                |
	| sentry             |
	+--------------------+
	8 rows in set (0.00 sec)	

	