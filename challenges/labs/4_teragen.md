The full teragen command and job output
```
[zhou@ip-172-31-30-195 root]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -D dfs.blocksize=64000000 10000000 /user/zhou/tgen
17/05/12 03:33:00 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-30-195.us-west-2.compute.internal/172.31.30.195:8032
17/05/12 03:33:01 INFO terasort.TeraSort: Generating 10000000 using 2
17/05/12 03:33:01 INFO mapreduce.JobSubmitter: number of splits:2
17/05/12 03:33:01 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494558459658_0002
17/05/12 03:33:02 INFO impl.YarnClientImpl: Submitted application application_1494558459658_0002
17/05/12 03:33:02 INFO mapreduce.Job: The url to track the job: http://ip-172-31-30-195.us-west-2.compute.internal:8088/proxy/application_1494558459658_0002/
17/05/12 03:33:02 INFO mapreduce.Job: Running job: job_1494558459658_0002
17/05/12 03:33:08 INFO mapreduce.Job: Job job_1494558459658_0002 running in uber mode : false
17/05/12 03:33:08 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 03:33:20 INFO mapreduce.Job:  map 38% reduce 0%
17/05/12 03:33:21 INFO mapreduce.Job:  map 78% reduce 0%
17/05/12 03:33:22 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 03:33:23 INFO mapreduce.Job: Job job_1494558459658_0002 completed successfully
17/05/12 03:33:23 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=247056
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=167
                HDFS: Number of bytes written=1000000000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=24535
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=24535
                Total vcore-seconds taken by all map tasks=24535
                Total megabyte-seconds taken by all map tasks=25123840
        Map-Reduce Framework
                Map input records=10000000
                Map output records=10000000
                Input split bytes=167
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=253
                CPU time spent (ms)=22260
                Physical memory (bytes) snapshot=757022720
                Virtual memory (bytes) snapshot=3164798976
                Total committed heap usage (bytes)=1156579328
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=21472776955442690
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=1000000000

				
real    0m25.713s
user    0m5.466s
sys     0m0.750s

```

The result of the time command
```

real    0m25.713s
user    0m5.466s
sys     0m0.750s

```

The command and output of hdfs dfs -ls /user/zhou/tgen 	
```
[zhou@ip-172-31-30-195 root]$ hdfs dfs -ls /user/zhou/tgen
Found 3 items
-rw-r--r--   3 zhou zhou          0 2017-05-12 03:33 /user/zhou/tgen/_SUCCESS
-rw-r--r--   3 zhou zhou  500000000 2017-05-12 03:33 /user/zhou/tgen/part-m-00000
-rw-r--r--   3 zhou zhou  500000000 2017-05-12 03:33 /user/zhou/tgen/part-m-00001
[zhou@ip-172-31-30-195 root]$

```
