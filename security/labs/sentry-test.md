```
[root@ip-172-31-35-111 java]# beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-35-111.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-35-111.us-west-2.compute.internal@HADOOP.COM
scan complete in 3ms
Connecting to jdbc:hive2://ip-172-31-35-111.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-35-111.us-west-2.compute.internal@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-35-111.us-west-2.co> show table
. . . . . . . . . . . . . . . . . . . . . . .> You have new mail in /var/spool/mail/root
[root@ip-172-31-35-111 java]# beeline
Beeline version 1.1.0-cdh5.9.2 by Apache Hive
beeline> !connect jdbc:hive2://ip-172-31-35-111.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-35-111.us-west-2.compute.internal@HADOOP.COM
scan complete in 3ms
Connecting to jdbc:hive2://ip-172-31-35-111.us-west-2.compute.internal:10000/default;principal=hive/ip-172-31-35-111.us-west-2.compute.internal@HADOOP.COM
Connected to: Apache Hive (version 1.1.0-cdh5.9.2)
Driver: Hive JDBC (version 1.1.0-cdh5.9.2)
Transaction isolation: TRANSACTION_REPEATABLE_READ
0: jdbc:hive2://ip-172-31-35-111.us-west-2.co> show tables;
INFO  : Compiling command(queryId=hive_20170511083535_06673422-d338-4bfd-a002-420ea629c943): show tables
INFO  : Semantic Analysis Completed
INFO  : Returning Hive schema: Schema(fieldSchemas:[FieldSchema(name:tab_name, type:string, comment:from deserializer)], properties:null)
INFO  : Completed compiling command(queryId=hive_20170511083535_06673422-d338-4bfd-a002-420ea629c943); Time taken: 0.649 seconds
INFO  : Executing command(queryId=hive_20170511083535_06673422-d338-4bfd-a002-420ea629c943): show tables
INFO  : Starting task [Stage-0:DDL] in serial mode
INFO  : Completed executing command(queryId=hive_20170511083535_06673422-d338-4bfd-a002-420ea629c943); Time taken: 0.423 seconds
INFO  : OK
+------------+--+
|  tab_name  |
+------------+--+
| customers  |
| sample_07  |
| sample_08  |
| web_logs   |
+------------+--+
4 rows selected (2.516 seconds)
0: jdbc:hive2://ip-172-31-35-111.us-west-2.co>

```
