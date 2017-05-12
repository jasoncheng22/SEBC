The full teragen command and job output
```
[zhou@ip-172-31-30-195 root]$ time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapreduce.map.memory.mb=1024 -Ddfs.blocksize=64000000 65536000 /user/zhou/tgen
17/05/12 03:37:00 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-30-195.us-west-2.compute.internal/172.31.30.195:8032
17/05/12 03:37:00 INFO terasort.TeraSort: Generating 65536000 using 2
17/05/12 03:37:00 INFO mapreduce.JobSubmitter: number of splits:2
17/05/12 03:37:00 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494558459658_0003
17/05/12 03:37:01 INFO impl.YarnClientImpl: Submitted application application_1494558459658_0003
17/05/12 03:37:01 INFO mapreduce.Job: The url to track the job: http://ip-172-31-30-195.us-west-2.compute.internal:8088/proxy/application_1494558459658_0003/
17/05/12 03:37:01 INFO mapreduce.Job: Running job: job_1494558459658_0003
17/05/12 03:37:08 INFO mapreduce.Job: Job job_1494558459658_0003 running in uber mode : false
17/05/12 03:37:08 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 03:37:19 INFO mapreduce.Job:  map 6% reduce 0%
17/05/12 03:37:20 INFO mapreduce.Job:  map 12% reduce 0%
17/05/12 03:37:22 INFO mapreduce.Job:  map 15% reduce 0%
17/05/12 03:37:23 INFO mapreduce.Job:  map 17% reduce 0%
17/05/12 03:37:25 INFO mapreduce.Job:  map 20% reduce 0%
17/05/12 03:37:26 INFO mapreduce.Job:  map 23% reduce 0%
17/05/12 03:37:28 INFO mapreduce.Job:  map 26% reduce 0%
17/05/12 03:37:29 INFO mapreduce.Job:  map 29% reduce 0%
17/05/12 03:37:31 INFO mapreduce.Job:  map 31% reduce 0%
17/05/12 03:37:32 INFO mapreduce.Job:  map 34% reduce 0%
17/05/12 03:37:34 INFO mapreduce.Job:  map 37% reduce 0%
17/05/12 03:37:35 INFO mapreduce.Job:  map 40% reduce 0%
17/05/12 03:37:37 INFO mapreduce.Job:  map 43% reduce 0%
17/05/12 03:37:38 INFO mapreduce.Job:  map 45% reduce 0%
17/05/12 03:37:40 INFO mapreduce.Job:  map 46% reduce 0%
17/05/12 03:37:41 INFO mapreduce.Job:  map 47% reduce 0%
17/05/12 03:37:43 INFO mapreduce.Job:  map 49% reduce 0%
17/05/12 03:37:44 INFO mapreduce.Job:  map 50% reduce 0%
17/05/12 03:37:46 INFO mapreduce.Job:  map 52% reduce 0%
17/05/12 03:37:47 INFO mapreduce.Job:  map 53% reduce 0%
17/05/12 03:37:50 INFO mapreduce.Job:  map 56% reduce 0%
17/05/12 03:37:53 INFO mapreduce.Job:  map 59% reduce 0%
17/05/12 03:37:56 INFO mapreduce.Job:  map 61% reduce 0%
17/05/12 03:37:59 INFO mapreduce.Job:  map 64% reduce 0%
17/05/12 03:38:02 INFO mapreduce.Job:  map 66% reduce 0%
17/05/12 03:38:05 INFO mapreduce.Job:  map 69% reduce 0%
17/05/12 03:38:08 INFO mapreduce.Job:  map 71% reduce 0%
17/05/12 03:38:11 INFO mapreduce.Job:  map 74% reduce 0%
17/05/12 03:38:14 INFO mapreduce.Job:  map 77% reduce 0%
17/05/12 03:38:17 INFO mapreduce.Job:  map 79% reduce 0%
17/05/12 03:38:20 INFO mapreduce.Job:  map 82% reduce 0%
17/05/12 03:38:23 INFO mapreduce.Job:  map 86% reduce 0%
17/05/12 03:38:26 INFO mapreduce.Job:  map 90% reduce 0%
17/05/12 03:38:29 INFO mapreduce.Job:  map 93% reduce 0%
17/05/12 03:38:32 INFO mapreduce.Job:  map 96% reduce 0%
17/05/12 03:38:35 INFO mapreduce.Job:  map 99% reduce 0%
17/05/12 03:38:37 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 03:38:37 INFO mapreduce.Job: Job job_1494558459658_0003 completed successfully
17/05/12 03:38:37 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=247066
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=170
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=8
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=4
        Job Counters
                Launched map tasks=2
                Other local map tasks=2
                Total time spent by all maps in occupied slots (ms)=173573
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=173573
                Total vcore-seconds taken by all map tasks=173573
                Total megabyte-seconds taken by all map tasks=177738752
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Input split bytes=170
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=710
                CPU time spent (ms)=97750
                Physical memory (bytes) snapshot=428605440
                Virtual memory (bytes) snapshot=3154026496
                Total committed heap usage (bytes)=770703360
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=140750829423462787
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=6553600000

real    1m40.518s
user    0m5.243s
sys     0m0.730s

```

The result of the time command
```

real    1m40.518s
user    0m5.243s
sys     0m0.730s

```

The command and output of hdfs dfs -ls /user/zhou/tgen 	
```
[zhou@ip-172-31-30-195 root]$ hdfs dfs -ls /user/zhou/tgen
Found 3 items
-rw-r--r--   3 zhou zhou          0 2017-05-12 03:38 /user/zhou/tgen/_SUCCESS
-rw-r--r--   3 zhou zhou 3276800000 2017-05-12 03:38 /user/zhou/tgen/part-m-00000
-rw-r--r--   3 zhou zhou 3276800000 2017-05-12 03:38 /user/zhou/tgen/part-m-00001

```
