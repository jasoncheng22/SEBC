# HDFS Lab: Test HDFS Snapshots
## List the commands and output for each step below in storage/labs/2_snapshot_test.md.

Create a precious directory in HDFS; copy the ZIP course file into it.
```
hadoop fs -mkdir -p /user/jasoncheng22/precious
hadoop fs -copyFromLocal ./SEBC-Shanghai.zip /user/jasoncheng22/precious

[jasoncheng22@ip-172-31-35-111 ~]$ hadoop fs -ls /user/jasoncheng22/precious
Found 1 items
-rw-r--r--   3 jasoncheng22 supergroup     474957 2017-05-09 08:23 /user/jasoncheng22/precious/SEBC-Shanghai.zip
```

Enable snapshots for precious
```
[root@ip-172-31-35-111 ~]# sudo -u hdfs hadoop dfsadmin -allowSnapshot /user/jasoncheng22/precious
DEPRECATED: Use of this script to execute hdfs command is deprecated.
Instead use the hdfs command for it.

Allowing snaphot on /user/jasoncheng22/precious succeeded
```

Create a snapshot called sebc-hdfs-test
```
[jasoncheng22@ip-172-31-35-111 /]$ hadoop fs -createSnapshot /user/jasoncheng22 sebc-hdfs-test
Created snapshot /user/jasoncheng22/precious/.snapshot/sebc-hdfs-test
```

Delete the directory
```
[jasoncheng22@ip-172-31-35-111 /]$ hadoop fs -rm -r /user/jasoncheng22/precious
rm: Failed to move to trash: hdfs://ip-172-31-36-117.us-west-2.compute.internal:8020/user/jasoncheng22/precious: The directory /user/jasoncheng22/precious cannot be deleted since /user/jasoncheng22/precious is snapshottable and already has snapshots
```

Delete the ZIP file
```
[jasoncheng22@ip-172-31-35-111 /]$ hadoop fs -rm /user/jasoncheng22/precious/SEBC-Shanghai.zip
17/05/09 08:37:22 INFO fs.TrashPolicyDefault: Moved: 'hdfs://ip-172-31-36-117.us-west-2.compute.internal:8020/user/jasoncheng22/precious/SEBC-Shanghai.zip' to trash at: hdfs://ip-172-31-36-117.us-west-2.compute.internal:8020/user/jasoncheng22/.Trash/Current/user/jasoncheng22/precious/SEBC-Shanghai.zip
```

Restore the deleted file
```
[jasoncheng22@ip-172-31-35-111 tmp]$ hadoop fs -cp /user/jasoncheng22/precious/.snapshot/sebc-hdfs-test/SEBC-Shanghai.zip /user/jasoncheng22/precious/
[jasoncheng22@ip-172-31-35-111 tmp]$ hadoop fs -ls /user/jasoncheng22/precious/
\Found 1 items
-rw-r--r--   3 jasoncheng22 supergroup     474957 2017-05-09 08:49 /user/jasoncheng22/precious/SEBC-Shanghai.zip
```


Capture the NameNode web UI screen that lists snapshots in storage/labs/2_snapshot_list.png.

