# HDFS Lab: Test HDFS throughput

Create an end-user Linux account named with your GitHub handle
```
useradd jasoncheng22
passwd jasoncheng22
```
Make sure this Linux account is added to all cluster nodes

Create an HDFS directory under /user
```
[jasoncheng22@ip-172-31-35-111 root]$ hadoop fs -mkdir jasoncheng22
[jasoncheng22@ip-172-31-35-111 root]$ hadoop fs -ls /user
Found 6 items
drwx------   - hdfs         supergroup          0 2017-05-09 05:38 /user/hdfs
drwxrwxrwx   - mapred       hadoop              0 2017-05-09 04:03 /user/history
drwxrwxr-t   - hive         hive                0 2017-05-09 04:03 /user/hive
drwxrwxr-x   - hue          hue                 0 2017-05-09 04:04 /user/hue
drwxr-xr-x   - jasoncheng22 supergroup          0 2017-05-09 07:04 /user/jasoncheng22
drwxrwxr-x   - oozie        oozie               0 2017-05-09 04:05 /user/oozie
```
Run the following exercises under this user account


# Create a 10 GB file using teragen
Set the number of mappers to four
Limit the block size to 32 MB
Land the output in your user's home directory
Use the time command to report the job's duration

```
[jasoncheng22@ip-172-31-35-111 tmp]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Ddfs.block.size=32768000 100000000 /user/jasoncheng22/input10GB
17/05/09 08:03:32 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-36-117.us-west-2.compute.internal/172.31.36.117:8032
17/05/09 08:03:32 INFO terasort.TeraSort: Generating 100000000 using 4
17/05/09 08:03:32 INFO mapreduce.JobSubmitter: number of splits:4
17/05/09 08:03:32 INFO Configuration.deprecation: mapred.map.tasks is deprecated. Instead, use mapreduce.job.maps
17/05/09 08:03:32 INFO Configuration.deprecation: dfs.block.size is deprecated. Instead, use dfs.blocksize
17/05/09 08:03:33 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494306356848_0010
17/05/09 08:03:33 INFO impl.YarnClientImpl: Submitted application application_1494306356848_0010
17/05/09 08:03:33 INFO mapreduce.Job: The url to track the job: http://ip-172-31-36-117.us-west-2.compute.internal:8088/proxy/application_1494306356848_0010/
17/05/09 08:03:33 INFO mapreduce.Job: Running job: job_1494306356848_0010
17/05/09 08:03:40 INFO mapreduce.Job: Job job_1494306356848_0010 running in uber mode : false
17/05/09 08:03:40 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 08:03:52 INFO mapreduce.Job:  map 3% reduce 0%
17/05/09 08:03:54 INFO mapreduce.Job:  map 8% reduce 0%
17/05/09 08:03:55 INFO mapreduce.Job:  map 10% reduce 0%
17/05/09 08:03:57 INFO mapreduce.Job:  map 13% reduce 0%
17/05/09 08:04:00 INFO mapreduce.Job:  map 17% reduce 0%
17/05/09 08:04:03 INFO mapreduce.Job:  map 20% reduce 0%
17/05/09 08:04:06 INFO mapreduce.Job:  map 22% reduce 0%
17/05/09 08:04:09 INFO mapreduce.Job:  map 24% reduce 0%
17/05/09 08:04:13 INFO mapreduce.Job:  map 27% reduce 0%
17/05/09 08:04:16 INFO mapreduce.Job:  map 29% reduce 0%
17/05/09 08:04:19 INFO mapreduce.Job:  map 31% reduce 0%
17/05/09 08:04:22 INFO mapreduce.Job:  map 34% reduce 0%
17/05/09 08:04:25 INFO mapreduce.Job:  map 36% reduce 0%
17/05/09 08:04:28 INFO mapreduce.Job:  map 38% reduce 0%
17/05/09 08:04:31 INFO mapreduce.Job:  map 40% reduce 0%
17/05/09 08:04:34 INFO mapreduce.Job:  map 42% reduce 0%
17/05/09 08:04:37 INFO mapreduce.Job:  map 45% reduce 0%
17/05/09 08:04:40 INFO mapreduce.Job:  map 48% reduce 0%
17/05/09 08:04:43 INFO mapreduce.Job:  map 50% reduce 0%
17/05/09 08:04:46 INFO mapreduce.Job:  map 53% reduce 0%
17/05/09 08:04:49 INFO mapreduce.Job:  map 55% reduce 0%
17/05/09 08:04:52 INFO mapreduce.Job:  map 57% reduce 0%
17/05/09 08:04:55 INFO mapreduce.Job:  map 60% reduce 0%
17/05/09 08:04:58 INFO mapreduce.Job:  map 61% reduce 0%
17/05/09 08:05:01 INFO mapreduce.Job:  map 63% reduce 0%
17/05/09 08:05:04 INFO mapreduce.Job:  map 65% reduce 0%
17/05/09 08:05:07 INFO mapreduce.Job:  map 67% reduce 0%
17/05/09 08:05:10 INFO mapreduce.Job:  map 70% reduce 0%
17/05/09 08:05:13 INFO mapreduce.Job:  map 72% reduce 0%
17/05/09 08:05:16 INFO mapreduce.Job:  map 75% reduce 0%
17/05/09 08:05:19 INFO mapreduce.Job:  map 77% reduce 0%
17/05/09 08:05:21 INFO mapreduce.Job:  map 78% reduce 0%
17/05/09 08:05:22 INFO mapreduce.Job:  map 79% reduce 0%
17/05/09 08:05:25 INFO mapreduce.Job:  map 81% reduce 0%
17/05/09 08:05:28 INFO mapreduce.Job:  map 83% reduce 0%
17/05/09 08:05:31 INFO mapreduce.Job:  map 85% reduce 0%
17/05/09 08:05:34 INFO mapreduce.Job:  map 87% reduce 0%
17/05/09 08:05:37 INFO mapreduce.Job:  map 88% reduce 0%
17/05/09 08:05:40 INFO mapreduce.Job:  map 90% reduce 0%
17/05/09 08:05:43 INFO mapreduce.Job:  map 92% reduce 0%
17/05/09 08:05:46 INFO mapreduce.Job:  map 94% reduce 0%
17/05/09 08:05:49 INFO mapreduce.Job:  map 96% reduce 0%
17/05/09 08:05:52 INFO mapreduce.Job:  map 98% reduce 0%
17/05/09 08:05:55 INFO mapreduce.Job:  map 99% reduce 0%
17/05/09 08:05:57 INFO mapreduce.Job:  map 100% reduce 0%
17/05/09 08:05:57 INFO mapreduce.Job: Job job_1494306356848_0010 completed successfully
17/05/09 08:05:57 INFO mapreduce.Job: Counters: 31
        File System Counters
                FILE: Number of bytes read=0
                FILE: Number of bytes written=494344
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=344
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=16
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=8
        Job Counters
                Launched map tasks=4
                Other local map tasks=4
                Total time spent by all maps in occupied slots (ms)=501863
                Total time spent by all reduces in occupied slots (ms)=0
                Total time spent by all map tasks (ms)=501863
                Total vcore-seconds taken by all map tasks=501863
                Total megabyte-seconds taken by all map tasks=513907712
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Input split bytes=344
                Spilled Records=0
                Failed Shuffles=0
                Merged Map outputs=0
                GC time elapsed (ms)=1557
                CPU time spent (ms)=161560
                Physical memory (bytes) snapshot=1026367488
                Virtual memory (bytes) snapshot=6254817280
                Total committed heap usage (bytes)=878706688
        org.apache.hadoop.examples.terasort.TeraGen$Counters
                CHECKSUM=214760662691937609
        File Input Format Counters
                Bytes Read=0
        File Output Format Counters
                Bytes Written=10000000000

real    2m29.220s
user    0m6.652s
sys     0m0.786s
```

Run the terasort command on this file
Use the time command to report the job's duration
Land the result under your user's home directory
```
time hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapred.reduce.tasks=50 /user/jasoncheng22/input10GB /user/jasoncheng22/input10GB-output
```

## Report your work in storage/labs/1_terasort_tests.md, including:
The full teragen and command you used and the job output
The same for terasort
Include the time result of each job
```
[jasoncheng22@ip-172-31-35-111 tmp]$ time hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapred.reduce.tasks=50 /user/jasoncheng22/input10GB /user/jasoncheng22/input10GB-output
17/05/09 08:13:10 INFO terasort.TeraSort: starting
17/05/09 08:13:11 INFO input.FileInputFormat: Total input paths to process : 4
Spent 245ms computing base-splits.
Spent 6ms computing TeraScheduler splits.
Computing input splits took 252ms
Sampling 10 splits of 308
Making 50 from 100000 sampled records
Computing parititions took 911ms
Spent 1165ms computing partitions.
17/05/09 08:13:12 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-36-117.us-west-2.compute.internal/172.31.36.117:8032
17/05/09 08:13:13 INFO mapreduce.JobSubmitter: number of splits:308
17/05/09 08:13:13 INFO Configuration.deprecation: mapred.reduce.tasks is deprecated. Instead, use mapreduce.job.reduces
17/05/09 08:13:13 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494306356848_0012
17/05/09 08:13:14 INFO impl.YarnClientImpl: Submitted application application_1494306356848_0012
17/05/09 08:13:14 INFO mapreduce.Job: The url to track the job: http://ip-172-31-36-117.us-west-2.compute.internal:8088/proxy/application_1494306356848_0012/
17/05/09 08:13:14 INFO mapreduce.Job: Running job: job_1494306356848_0012
17/05/09 08:13:21 INFO mapreduce.Job: Job job_1494306356848_0012 running in uber mode : false
17/05/09 08:13:21 INFO mapreduce.Job:  map 0% reduce 0%
17/05/09 08:13:31 INFO mapreduce.Job:  map 1% reduce 0%
17/05/09 08:13:33 INFO mapreduce.Job:  map 2% reduce 0%
17/05/09 08:13:36 INFO mapreduce.Job:  map 4% reduce 0%
17/05/09 08:13:40 INFO mapreduce.Job:  map 5% reduce 0%
17/05/09 08:13:43 INFO mapreduce.Job:  map 6% reduce 0%
17/05/09 08:13:49 INFO mapreduce.Job:  map 7% reduce 0%
17/05/09 08:13:50 INFO mapreduce.Job:  map 9% reduce 0%
17/05/09 08:13:54 INFO mapreduce.Job:  map 10% reduce 0%
17/05/09 08:13:58 INFO mapreduce.Job:  map 11% reduce 0%
17/05/09 08:14:04 INFO mapreduce.Job:  map 14% reduce 0%
17/05/09 08:14:07 INFO mapreduce.Job:  map 15% reduce 0%
17/05/09 08:14:15 INFO mapreduce.Job:  map 16% reduce 0%
17/05/09 08:14:16 INFO mapreduce.Job:  map 17% reduce 0%
17/05/09 08:14:17 INFO mapreduce.Job:  map 18% reduce 0%
17/05/09 08:14:18 INFO mapreduce.Job:  map 19% reduce 0%
17/05/09 08:14:25 INFO mapreduce.Job:  map 21% reduce 0%
17/05/09 08:14:32 INFO mapreduce.Job:  map 23% reduce 0%
17/05/09 08:14:33 INFO mapreduce.Job:  map 24% reduce 0%
17/05/09 08:14:35 INFO mapreduce.Job:  map 25% reduce 0%
17/05/09 08:14:44 INFO mapreduce.Job:  map 26% reduce 0%
17/05/09 08:14:46 INFO mapreduce.Job:  map 27% reduce 0%
17/05/09 08:14:47 INFO mapreduce.Job:  map 29% reduce 0%
17/05/09 08:14:52 INFO mapreduce.Job:  map 30% reduce 0%
17/05/09 08:14:57 INFO mapreduce.Job:  map 31% reduce 0%
17/05/09 08:15:00 INFO mapreduce.Job:  map 32% reduce 0%
17/05/09 08:15:01 INFO mapreduce.Job:  map 34% reduce 0%
17/05/09 08:15:07 INFO mapreduce.Job:  map 35% reduce 0%
17/05/09 08:15:10 INFO mapreduce.Job:  map 36% reduce 0%
17/05/09 08:15:14 INFO mapreduce.Job:  map 37% reduce 0%
17/05/09 08:15:15 INFO mapreduce.Job:  map 39% reduce 0%
17/05/09 08:15:18 INFO mapreduce.Job:  map 40% reduce 0%
17/05/09 08:15:25 INFO mapreduce.Job:  map 41% reduce 0%
17/05/09 08:15:28 INFO mapreduce.Job:  map 42% reduce 0%
17/05/09 08:15:29 INFO mapreduce.Job:  map 44% reduce 0%
17/05/09 08:15:34 INFO mapreduce.Job:  map 45% reduce 0%
17/05/09 08:15:38 INFO mapreduce.Job:  map 46% reduce 0%
17/05/09 08:15:42 INFO mapreduce.Job:  map 48% reduce 0%
17/05/09 08:15:43 INFO mapreduce.Job:  map 49% reduce 0%
17/05/09 08:15:47 INFO mapreduce.Job:  map 50% reduce 0%
17/05/09 08:15:52 INFO mapreduce.Job:  map 51% reduce 0%
17/05/09 08:15:55 INFO mapreduce.Job:  map 52% reduce 0%
17/05/09 08:15:56 INFO mapreduce.Job:  map 53% reduce 0%
17/05/09 08:15:57 INFO mapreduce.Job:  map 54% reduce 0%
17/05/09 08:15:58 INFO mapreduce.Job:  map 55% reduce 0%
17/05/09 08:16:06 INFO mapreduce.Job:  map 56% reduce 0%
17/05/09 08:16:08 INFO mapreduce.Job:  map 57% reduce 0%
17/05/09 08:16:09 INFO mapreduce.Job:  map 58% reduce 0%
17/05/09 08:16:11 INFO mapreduce.Job:  map 59% reduce 0%
17/05/09 08:16:14 INFO mapreduce.Job:  map 60% reduce 0%
17/05/09 08:16:18 INFO mapreduce.Job:  map 61% reduce 0%
17/05/09 08:16:21 INFO mapreduce.Job:  map 62% reduce 0%
17/05/09 08:16:24 INFO mapreduce.Job:  map 63% reduce 0%
17/05/09 08:16:25 INFO mapreduce.Job:  map 64% reduce 0%
17/05/09 08:16:27 INFO mapreduce.Job:  map 65% reduce 0%
17/05/09 08:16:33 INFO mapreduce.Job:  map 66% reduce 0%
17/05/09 08:16:34 INFO mapreduce.Job:  map 67% reduce 0%
17/05/09 08:16:39 INFO mapreduce.Job:  map 69% reduce 0%
17/05/09 08:16:42 INFO mapreduce.Job:  map 70% reduce 0%
17/05/09 08:16:47 INFO mapreduce.Job:  map 71% reduce 0%
17/05/09 08:16:48 INFO mapreduce.Job:  map 72% reduce 0%
17/05/09 08:16:50 INFO mapreduce.Job:  map 73% reduce 0%
17/05/09 08:16:53 INFO mapreduce.Job:  map 74% reduce 0%
17/05/09 08:16:56 INFO mapreduce.Job:  map 75% reduce 0%
17/05/09 08:16:59 INFO mapreduce.Job:  map 76% reduce 0%
17/05/09 08:17:01 INFO mapreduce.Job:  map 77% reduce 0%
17/05/09 08:17:04 INFO mapreduce.Job:  map 78% reduce 0%
17/05/09 08:17:06 INFO mapreduce.Job:  map 79% reduce 0%
17/05/09 08:17:09 INFO mapreduce.Job:  map 80% reduce 0%
17/05/09 08:17:12 INFO mapreduce.Job:  map 81% reduce 0%
17/05/09 08:17:14 INFO mapreduce.Job:  map 82% reduce 0%
17/05/09 08:17:19 INFO mapreduce.Job:  map 83% reduce 0%
17/05/09 08:17:20 INFO mapreduce.Job:  map 84% reduce 0%
17/05/09 08:17:23 INFO mapreduce.Job:  map 85% reduce 0%
17/05/09 08:17:25 INFO mapreduce.Job:  map 85% reduce 1%
17/05/09 08:17:29 INFO mapreduce.Job:  map 85% reduce 2%
17/05/09 08:17:30 INFO mapreduce.Job:  map 86% reduce 3%
17/05/09 08:17:34 INFO mapreduce.Job:  map 87% reduce 3%
17/05/09 08:17:36 INFO mapreduce.Job:  map 87% reduce 5%
17/05/09 08:17:37 INFO mapreduce.Job:  map 88% reduce 5%
17/05/09 08:17:42 INFO mapreduce.Job:  map 89% reduce 5%
17/05/09 08:17:46 INFO mapreduce.Job:  map 90% reduce 5%
17/05/09 08:17:50 INFO mapreduce.Job:  map 91% reduce 5%
17/05/09 08:17:55 INFO mapreduce.Job:  map 92% reduce 5%
17/05/09 08:17:58 INFO mapreduce.Job:  map 93% reduce 5%
17/05/09 08:18:05 INFO mapreduce.Job:  map 94% reduce 5%
17/05/09 08:18:11 INFO mapreduce.Job:  map 95% reduce 5%
17/05/09 08:18:12 INFO mapreduce.Job:  map 96% reduce 5%
17/05/09 08:18:18 INFO mapreduce.Job:  map 97% reduce 5%
17/05/09 08:18:21 INFO mapreduce.Job:  map 98% reduce 5%
17/05/09 08:18:26 INFO mapreduce.Job:  map 99% reduce 5%
17/05/09 08:18:32 INFO mapreduce.Job:  map 100% reduce 5%
17/05/09 08:18:33 INFO mapreduce.Job:  map 100% reduce 6%
17/05/09 08:18:35 INFO mapreduce.Job:  map 100% reduce 7%
17/05/09 08:18:36 INFO mapreduce.Job:  map 100% reduce 10%
17/05/09 08:18:38 INFO mapreduce.Job:  map 100% reduce 11%
17/05/09 08:18:40 INFO mapreduce.Job:  map 100% reduce 13%
17/05/09 08:18:41 INFO mapreduce.Job:  map 100% reduce 16%
17/05/09 08:18:43 INFO mapreduce.Job:  map 100% reduce 18%
17/05/09 08:18:44 INFO mapreduce.Job:  map 100% reduce 20%
17/05/09 08:18:45 INFO mapreduce.Job:  map 100% reduce 21%
17/05/09 08:18:46 INFO mapreduce.Job:  map 100% reduce 22%
17/05/09 08:18:47 INFO mapreduce.Job:  map 100% reduce 23%
17/05/09 08:18:48 INFO mapreduce.Job:  map 100% reduce 25%
17/05/09 08:18:53 INFO mapreduce.Job:  map 100% reduce 27%
17/05/09 08:18:56 INFO mapreduce.Job:  map 100% reduce 30%
17/05/09 08:18:57 INFO mapreduce.Job:  map 100% reduce 32%
17/05/09 08:19:00 INFO mapreduce.Job:  map 100% reduce 35%
17/05/09 08:19:01 INFO mapreduce.Job:  map 100% reduce 37%
17/05/09 08:19:02 INFO mapreduce.Job:  map 100% reduce 41%
17/05/09 08:19:03 INFO mapreduce.Job:  map 100% reduce 42%
17/05/09 08:19:05 INFO mapreduce.Job:  map 100% reduce 45%
17/05/09 08:19:06 INFO mapreduce.Job:  map 100% reduce 46%
17/05/09 08:19:07 INFO mapreduce.Job:  map 100% reduce 47%
17/05/09 08:19:08 INFO mapreduce.Job:  map 100% reduce 48%
17/05/09 08:19:09 INFO mapreduce.Job:  map 100% reduce 49%
17/05/09 08:19:11 INFO mapreduce.Job:  map 100% reduce 51%
17/05/09 08:19:12 INFO mapreduce.Job:  map 100% reduce 52%
17/05/09 08:19:14 INFO mapreduce.Job:  map 100% reduce 54%
17/05/09 08:19:15 INFO mapreduce.Job:  map 100% reduce 56%
17/05/09 08:19:17 INFO mapreduce.Job:  map 100% reduce 59%
17/05/09 08:19:18 INFO mapreduce.Job:  map 100% reduce 60%
17/05/09 08:19:20 INFO mapreduce.Job:  map 100% reduce 61%
17/05/09 08:19:22 INFO mapreduce.Job:  map 100% reduce 62%
17/05/09 08:19:23 INFO mapreduce.Job:  map 100% reduce 63%
17/05/09 08:19:24 INFO mapreduce.Job:  map 100% reduce 64%
17/05/09 08:19:26 INFO mapreduce.Job:  map 100% reduce 65%
17/05/09 08:19:27 INFO mapreduce.Job:  map 100% reduce 69%
17/05/09 08:19:29 INFO mapreduce.Job:  map 100% reduce 70%
17/05/09 08:19:30 INFO mapreduce.Job:  map 100% reduce 72%
17/05/09 08:19:31 INFO mapreduce.Job:  map 100% reduce 75%
17/05/09 08:19:33 INFO mapreduce.Job:  map 100% reduce 76%
17/05/09 08:19:34 INFO mapreduce.Job:  map 100% reduce 77%
17/05/09 08:19:35 INFO mapreduce.Job:  map 100% reduce 80%
17/05/09 08:19:36 INFO mapreduce.Job:  map 100% reduce 81%
17/05/09 08:19:37 INFO mapreduce.Job:  map 100% reduce 83%
17/05/09 08:19:38 INFO mapreduce.Job:  map 100% reduce 85%
17/05/09 08:19:39 INFO mapreduce.Job:  map 100% reduce 87%
17/05/09 08:19:40 INFO mapreduce.Job:  map 100% reduce 88%
17/05/09 08:19:41 INFO mapreduce.Job:  map 100% reduce 89%
17/05/09 08:19:44 INFO mapreduce.Job:  map 100% reduce 91%
17/05/09 08:19:47 INFO mapreduce.Job:  map 100% reduce 92%
17/05/09 08:19:49 INFO mapreduce.Job:  map 100% reduce 94%
17/05/09 08:19:50 INFO mapreduce.Job:  map 100% reduce 95%
17/05/09 08:19:51 INFO mapreduce.Job:  map 100% reduce 97%
17/05/09 08:19:52 INFO mapreduce.Job:  map 100% reduce 99%
17/05/09 08:19:53 INFO mapreduce.Job:  map 100% reduce 100%
17/05/09 08:19:54 INFO mapreduce.Job: Job job_1494306356848_0012 completed successfully
17/05/09 08:19:54 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=4462012868
                FILE: Number of bytes written=8882738924
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=10000049588
                HDFS: Number of bytes written=10000000000
                HDFS: Number of read operations=1074
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=100
        Job Counters
                Launched map tasks=308
                Launched reduce tasks=50
                Data-local map tasks=305
                Rack-local map tasks=3
                Total time spent by all maps in occupied slots (ms)=3058479
                Total time spent by all reduces in occupied slots (ms)=1506958
                Total time spent by all map tasks (ms)=3058479
                Total time spent by all reduce tasks (ms)=1506958
                Total vcore-seconds taken by all map tasks=3058479
                Total vcore-seconds taken by all reduce tasks=1506958
                Total megabyte-seconds taken by all map tasks=3131882496
                Total megabyte-seconds taken by all reduce tasks=1543124992
        Map-Reduce Framework
                Map input records=100000000
                Map output records=100000000
                Map output bytes=10200000000
                Map output materialized bytes=4375765954
                Input split bytes=49588
                Combine input records=0
                Combine output records=0
                Reduce input groups=100000000
                Reduce shuffle bytes=4375765954
                Reduce input records=100000000
                Reduce output records=100000000
                Spilled Records=200000000
                Shuffled Maps =15400
                Failed Shuffles=0
                Merged Map outputs=15400
                GC time elapsed (ms)=60164
                CPU time spent (ms)=1878690
                Physical memory (bytes) snapshot=172824064000
                Virtual memory (bytes) snapshot=560544452608
                Total committed heap usage (bytes)=194702737408
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=10000000000
        File Output Format Counters
                Bytes Written=10000000000
17/05/09 08:19:54 INFO terasort.TeraSort: done

real    6m45.570s
user    0m9.741s
sys     0m0.979s

```
