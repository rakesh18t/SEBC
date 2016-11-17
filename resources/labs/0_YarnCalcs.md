Worker vcores	12
Worker spindles	3
Worker RAM	45
Workload factor	2
Worker nodes	3

reduced o/s memory to 8% of total worker RAM

map and reduce jobs will remain a value of 6 which is the maximum no of vcores available. if the threshold drops (workload factor 1) the number of jobs drops to 3

as vCores are assigned (impalad, HBase, Solr) this reduces performance on the worker nodes thus reducinging the number of jobs that can be run.