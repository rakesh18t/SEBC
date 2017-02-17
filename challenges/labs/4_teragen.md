4_teragen.md

[root@ip-172-31-22-220 jars]# su hdfs
[hdfs@ip-172-31-22-220 jars]$  hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.10.0.jar teragen -D dfs.blocksize=96m -D mapred.map.tasks=4 51200000 /user/raffles/tgen512m
17/02/17 18:59:00 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-22-220.us-west-1.compute.internal/172.31.22.220:8032
17/02/17 18:59:01 INFO terasort.TeraGen: Generating 51200000 using 4
17/02/17 18:59:01 INFO mapreduce.JobSubmitter: number of splits:4
17/02/17 18:59:01 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/02/17 18:59:01 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1487317976933_0001
17/02/17 18:59:02 INFO impl.YarnClientImpl: Submitted application application_1487317976933_0001
17/02/17 18:59:02 INFO mapreduce.Job: The url to track the job: http://ip-172-31-22-220.us-west-1.compute.internal:8088/proxy/application_1487317976933_0001/
17/02/17 18:59:02 INFO mapreduce.Job: Running job: job_1487317976933_0001
17/02/17 18:59:08 INFO mapreduce.Job: Job job_1487317976933_0001 running in uber mode : false
17/02/17 18:59:08 INFO mapreduce.Job:  map 0% reduce 0%
^C[hdfs@ip-172-31-22-220 jars]$ time  hadoop jar hadoop-mapreduce-examples-2.6.0-cdh5.10.0.jar teragen -D dfs.blocksize=96m -D mapred.map.tasks=4 51200000 /user/raffles/tgen512m
java.io.IOException: Output directory /user/raffles/tgen512m already exists.
        at org.apache.hadoop.examples.terasort.TeraGen.run(TeraGen.java:293)
        at org.apache.hadoop.util.ToolRunner.run(ToolRunner.java:70)
        at org.apache.hadoop.examples.terasort.TeraGen.main(TeraGen.java:309)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.ProgramDriver$ProgramDescription.invoke(ProgramDriver.java:71)
        at org.apache.hadoop.util.ProgramDriver.run(ProgramDriver.java:144)
        at org.apache.hadoop.examples.ExampleDriver.main(ExampleDriver.java:74)
        at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
        at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:57)
        at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
        at java.lang.reflect.Method.invoke(Method.java:606)
        at org.apache.hadoop.util.RunJar.run(RunJar.java:221)
        at org.apache.hadoop.util.RunJar.main(RunJar.java:136)

real    0m2.424s
user    0m3.278s
sys     0m0.164s
