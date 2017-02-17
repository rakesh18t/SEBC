3_cm.md

[root@ip-172-31-22-220 etc]# su hdfs
[hdfs@ip-172-31-22-220 etc]$ hdfs dfs -mkdir /user/raffles
[hdfs@ip-172-31-22-220 etc]$ hdfs dfs -mkdir /user/fullerton
[hdfs@ip-172-31-22-220 etc]$ hdfs dfs -ls /user
Found 6 items
drwxr-xr-x   - hdfs   supergroup          0 2017-02-17 18:47 /user/fullerton
drwxrwxrwx   - mapred hadoop              0 2017-02-17 16:52 /user/history
drwxrwxr-t   - hive   hive                0 2017-02-17 16:53 /user/hive
drwxrwxr-x   - hue    hue                 0 2017-02-17 16:54 /user/hue
drwxrwxr-x   - oozie  oozie               0 2017-02-17 16:54 /user/oozie
drwxr-xr-x   - hdfs   supergroup          0 2017-02-17 18:46 /user/raffles
[hdfs@ip-172-31-22-220 etc]$
