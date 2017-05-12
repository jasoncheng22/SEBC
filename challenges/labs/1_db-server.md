The hostname of your database server
```
[root@ip-172-31-17-68 ~]# hostname -f
ip-172-31-17-68.us-west-2.compute.internal
```

The command and output for showing the database server version
```
mysql> SELECT VERSION();
+-----------+
| VERSION() |
+-----------+
| 5.6.36    |
+-----------+
1 row in set (0.00 sec)

```

The command and output for listing the databases created above

```
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
+--------------------+
9 rows in set (0.00 sec)
```
