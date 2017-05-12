```
[zhou@ip-172-31-30-195 root]$ hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort /user/zhou/tgen /user/zhou/tsort
17/05/12 04:22:19 INFO terasort.TeraSort: starting
17/05/12 04:22:21 INFO hdfs.DFSClient: Created token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@JASONCHENG22.AU, renewer=yarn, realUser=, issueDate=1494562941478, maxDate=1495167741478, sequenceNumber=2, masterKeyId=2 on 172.31.30.195:8020
17/05/12 04:22:21 INFO security.TokenCache: Got dt for hdfs://ip-172-31-30-195.us-west-2.compute.internal:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.30.195:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@JASONCHENG22.AU, renewer=yarn, realUser=, issueDate=1494562941478, maxDate=1495167741478, sequenceNumber=2, masterKeyId=2)
17/05/12 04:22:21 INFO input.FileInputFormat: Total input paths to process : 2
Spent 350ms computing base-splits.
Spent 4ms computing TeraScheduler splits.
Computing input splits took 355ms
Sampling 10 splits of 104
Making 20 from 100000 sampled records
Computing parititions took 732ms
Spent 1090ms computing partitions.
17/05/12 04:22:22 INFO client.RMProxy: Connecting to ResourceManager at ip-172-31-30-195.us-west-2.compute.internal/172.31.30.195:8032
17/05/12 04:22:22 INFO mapreduce.JobSubmitter: number of splits:104
17/05/12 04:22:23 INFO mapreduce.JobSubmitter: Submitting tokens for job: job_1494562347927_0002
17/05/12 04:22:23 INFO mapreduce.JobSubmitter: Kind: HDFS_DELEGATION_TOKEN, Service: 172.31.30.195:8020, Ident: (token for zhou: HDFS_DELEGATION_TOKEN owner=zhou@JASONCHENG22.AU, renewer=yarn, realUser=, issueDate=1494562941478, maxDate=1495167741478, sequenceNumber=2, masterKeyId=2)
17/05/12 04:22:23 INFO impl.YarnClientImpl: Submitted application application_1494562347927_0002
17/05/12 04:22:23 INFO mapreduce.Job: The url to track the job: http://ip-172-31-30-195.us-west-2.compute.internal:8088/proxy/application_1494562347927_0002/
17/05/12 04:22:23 INFO mapreduce.Job: Running job: job_1494562347927_0002
17/05/12 04:22:32 INFO mapreduce.Job: Job job_1494562347927_0002 running in uber mode : false
17/05/12 04:22:32 INFO mapreduce.Job:  map 0% reduce 0%
17/05/12 04:22:44 INFO mapreduce.Job:  map 1% reduce 0%
17/05/12 04:22:47 INFO mapreduce.Job:  map 5% reduce 0%
17/05/12 04:22:48 INFO mapreduce.Job:  map 8% reduce 0%
17/05/12 04:22:51 INFO mapreduce.Job:  map 9% reduce 0%
17/05/12 04:22:52 INFO mapreduce.Job:  map 14% reduce 0%
17/05/12 04:22:53 INFO mapreduce.Job:  map 17% reduce 0%
17/05/12 04:22:54 INFO mapreduce.Job:  map 22% reduce 0%
17/05/12 04:22:55 INFO mapreduce.Job:  map 28% reduce 0%
17/05/12 04:22:56 INFO mapreduce.Job:  map 30% reduce 0%
17/05/12 04:22:58 INFO mapreduce.Job:  map 31% reduce 0%
17/05/12 04:23:01 INFO mapreduce.Job:  map 33% reduce 0%
17/05/12 04:23:02 INFO mapreduce.Job:  map 35% reduce 0%
17/05/12 04:23:03 INFO mapreduce.Job:  map 38% reduce 0%
17/05/12 04:23:06 INFO mapreduce.Job:  map 39% reduce 0%
17/05/12 04:23:07 INFO mapreduce.Job:  map 44% reduce 0%
17/05/12 04:23:08 INFO mapreduce.Job:  map 48% reduce 0%
17/05/12 04:23:09 INFO mapreduce.Job:  map 53% reduce 0%
17/05/12 04:23:12 INFO mapreduce.Job:  map 59% reduce 0%
17/05/12 04:23:13 INFO mapreduce.Job:  map 60% reduce 0%
17/05/12 04:23:14 INFO mapreduce.Job:  map 62% reduce 0%
17/05/12 04:23:15 INFO mapreduce.Job:  map 64% reduce 0%
17/05/12 04:23:16 INFO mapreduce.Job:  map 67% reduce 0%
17/05/12 04:23:18 INFO mapreduce.Job:  map 68% reduce 0%
17/05/12 04:23:19 INFO mapreduce.Job:  map 69% reduce 0%
17/05/12 04:23:20 INFO mapreduce.Job:  map 72% reduce 0%
17/05/12 04:23:21 INFO mapreduce.Job:  map 77% reduce 0%
17/05/12 04:23:22 INFO mapreduce.Job:  map 81% reduce 0%
17/05/12 04:23:23 INFO mapreduce.Job:  map 82% reduce 0%
17/05/12 04:23:24 INFO mapreduce.Job:  map 83% reduce 0%
17/05/12 04:23:27 INFO mapreduce.Job:  map 88% reduce 0%
17/05/12 04:23:28 INFO mapreduce.Job:  map 95% reduce 0%
17/05/12 04:23:29 INFO mapreduce.Job:  map 98% reduce 0%
17/05/12 04:23:30 INFO mapreduce.Job:  map 100% reduce 0%
17/05/12 04:23:34 INFO mapreduce.Job:  map 100% reduce 3%
17/05/12 04:23:36 INFO mapreduce.Job:  map 100% reduce 5%
17/05/12 04:23:37 INFO mapreduce.Job:  map 100% reduce 21%
17/05/12 04:23:38 INFO mapreduce.Job:  map 100% reduce 30%
17/05/12 04:23:39 INFO mapreduce.Job:  map 100% reduce 36%
17/05/12 04:23:40 INFO mapreduce.Job:  map 100% reduce 40%
17/05/12 04:23:41 INFO mapreduce.Job:  map 100% reduce 44%
17/05/12 04:23:42 INFO mapreduce.Job:  map 100% reduce 51%
17/05/12 04:23:43 INFO mapreduce.Job:  map 100% reduce 62%
17/05/12 04:23:44 INFO mapreduce.Job:  map 100% reduce 66%
17/05/12 04:23:45 INFO mapreduce.Job:  map 100% reduce 72%
17/05/12 04:23:46 INFO mapreduce.Job:  map 100% reduce 75%
17/05/12 04:23:47 INFO mapreduce.Job:  map 100% reduce 80%
17/05/12 04:23:48 INFO mapreduce.Job:  map 100% reduce 83%
17/05/12 04:23:49 INFO mapreduce.Job:  map 100% reduce 85%
17/05/12 04:23:50 INFO mapreduce.Job:  map 100% reduce 87%
17/05/12 04:23:51 INFO mapreduce.Job:  map 100% reduce 90%
17/05/12 04:23:52 INFO mapreduce.Job:  map 100% reduce 91%
17/05/12 04:23:53 INFO mapreduce.Job:  map 100% reduce 92%
17/05/12 04:23:54 INFO mapreduce.Job:  map 100% reduce 93%
17/05/12 04:23:55 INFO mapreduce.Job:  map 100% reduce 95%
17/05/12 04:23:57 INFO mapreduce.Job:  map 100% reduce 98%
17/05/12 04:23:58 INFO mapreduce.Job:  map 100% reduce 99%
17/05/12 04:23:59 INFO mapreduce.Job:  map 100% reduce 100%
17/05/12 04:23:59 INFO mapreduce.Job: Job job_1494562347927_0002 completed successfully
17/05/12 04:23:59 INFO mapreduce.Job: Counters: 50
        File System Counters
                FILE: Number of bytes read=2924239399
                FILE: Number of bytes written=5812770283
                FILE: Number of read operations=0
                FILE: Number of large read operations=0
                FILE: Number of write operations=0
                HDFS: Number of bytes read=6553615392
                HDFS: Number of bytes written=6553600000
                HDFS: Number of read operations=372
                HDFS: Number of large read operations=0
                HDFS: Number of write operations=40
        Job Counters
                Launched map tasks=104
                Launched reduce tasks=20
                Data-local map tasks=102
                Rack-local map tasks=2
                Total time spent by all maps in occupied slots (ms)=1421475
                Total time spent by all reduces in occupied slots (ms)=495313
                Total time spent by all map tasks (ms)=1421475
                Total time spent by all reduce tasks (ms)=495313
                Total vcore-seconds taken by all map tasks=1421475
                Total vcore-seconds taken by all reduce tasks=495313
                Total megabyte-seconds taken by all map tasks=1455590400
                Total megabyte-seconds taken by all reduce tasks=507200512
        Map-Reduce Framework
                Map input records=65536000
                Map output records=65536000
                Map output bytes=6684672000
                Map output materialized bytes=2872918892
                Input split bytes=15392
                Combine input records=0
                Combine output records=0
                Reduce input groups=65536000
                Reduce shuffle bytes=2872918892
                Reduce input records=65536000
                Reduce output records=65536000
                Spilled Records=131072000
                Shuffled Maps =2080
                Failed Shuffles=0
                Merged Map outputs=2080
                GC time elapsed (ms)=24539
                CPU time spent (ms)=906940
                Physical memory (bytes) snapshot=69685047296
                Virtual memory (bytes) snapshot=196131864576
                Total committed heap usage (bytes)=65732608000
        Shuffle Errors
                BAD_ID=0
                CONNECTION=0
                IO_ERROR=0
                WRONG_LENGTH=0
                WRONG_MAP=0
                WRONG_REDUCE=0
        File Input Format Counters
                Bytes Read=6553600000
        File Output Format Counters
                Bytes Written=6553600000
17/05/12 04:23:59 INFO terasort.TeraSort: done

```