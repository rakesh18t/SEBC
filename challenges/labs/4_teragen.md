4_teragen.md


time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-mapreduce/hadoop-mapreduce-examples-2.6.0-cdh5.10.1.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=96m 51200000 /user/raffles/tgen512m

real    2m6.620s
user    1m48.681s
sys     0m6.485s

