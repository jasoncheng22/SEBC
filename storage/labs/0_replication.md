### dfrdsjk

HDFS Lab: Replicate to another cluster

Node: Data replication in the cloud depends on peers that can see each other's nodes.

Choose a partner in class
Name a source directory after your GitHub handle
```
[root@ip-172-31-45-227 ~]# sudo -u hdfs hadoop fs -mkdir /jasoncheng22
```

Name a target directory after your partner's GitHub handle
```
[root@ip-172-31-45-227 ~]# sudo -u hdfs hadoop fs -mkdir /vlin3
```

Use teragen to create a 500 MB file
```
[root@ip-172-31-45-227 ~]# sudo -u hdfs hadoop jar /opt/cloudera/parcels/CDH-5.9.2-1.cdh5.9.2.p0.3/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen 5000000 /jasoncheng22/input500MB

```

Copy your partner's file to your target directory


Let one partner use distCp on the command line
```
sudo -u hdfs hadoop distcp hdfs://ec2-54-148-197-198.us-west-2.compute.amazonaws.com/vlin3/ /
```
Let the other use BDR
```

```
Browse the results
Use hdfs fsck <path> -files -blocks on your source and target directories
```
hdfs fsck /jasoncheng22 -files -blocks
```

```
hdfs fsck /vlin3 -files -blocks

[root@ip-172-31-35-111 ~]# hdfs fsck /vlin3 -files -blocks
Connecting to namenode via http://ip-172-31-36-117.us-west-2.compute.internal:50070
FSCK started by root (auth:SIMPLE) from /172.31.35.111 for path /vlin3 at Tue May 09 07:01:45 UTC 2017
/vlin3 <dir>
/vlin3/input500MB <dir>
/vlin3/input500MB/_SUCCESS 0 bytes, 0 block(s):  OK

/vlin3/input500MB/part-m-00000 250000000 bytes, 2 block(s):  OK
0. BP-2046751524-172.31.36.117-1494302518851:blk_1073742756_1932 len=134217728 Live_repl=3
1. BP-2046751524-172.31.36.117-1494302518851:blk_1073742759_1935 len=115782272 Live_repl=3

/vlin3/input500MB/part-m-00001 250000000 bytes, 2 block(s):  OK
0. BP-2046751524-172.31.36.117-1494302518851:blk_1073742755_1931 len=134217728 Live_repl=3
1. BP-2046751524-172.31.36.117-1494302518851:blk_1073742758_1934 len=115782272 Live_repl=3

Status: HEALTHY
 Total size:    500000000 B
 Total dirs:    2
 Total files:   3
 Total symlinks:                0
 Total blocks (validated):      4 (avg. block size 125000000 B)
 Minimally replicated blocks:   4 (100.0 %)
 Over-replicated blocks:        0 (0.0 %)
 Under-replicated blocks:       0 (0.0 %)
 Mis-replicated blocks:         0 (0.0 %)
 Default replication factor:    3
 Average block replication:     3.0
 Corrupt blocks:                0
 Missing replicas:              0 (0.0 %)
 Number of data-nodes:          5
 Number of racks:               1
FSCK ended at Tue May 09 07:01:45 UTC 2017 in 2 milliseconds


The filesystem under path '/vlin3' is HEALTHY

```


Copy the work for this lab into storage/labs/0_replication.md


