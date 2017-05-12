List the command and output for ls /etc/yum.repos.d
```
[root@ip-172-31-17-68 ~]# ls /etc/yum.repos.d
CentOS-Base.repo  CentOS-Debuginfo.repo  CentOS-Media.repo  CentOS-Vault.repo  cloudera-manager.repo  mysql-community.repo
```


Connect Cloudera Manager Server to its database
Use the scm_prepare_database.sh script to create the db.properties file
List the full command and result in 2_cm.md
```
[root@ip-172-31-30-195 ~]# sudo /usr/share/cmf/schema/scm_prepare_database.sh mysql -h ip-172-31-17-68.us-west-2.compute.internal -utemp -ptemp --scm-host ip-172-31-30-195.us-west-2.compute.internal scm scm scm
JAVA_HOME=/usr/java/jdk1.7.0_67-cloudera
Verifying that we can write to /etc/cloudera-scm-server
Creating SCM configuration file in /etc/cloudera-scm-server
Executing:  /usr/java/jdk1.7.0_67-cloudera/bin/java -cp /usr/share/java/mysql-connector-java.jar:/usr/share/java/oracle-connector-java.jar:/usr/share/cmf/schema/../lib/* com.cloudera.enterprise.dbutil.DbCommandExecutor /etc/cloudera-scm-server/db.properties com.cloudera.cmf.db.
[                          main] DbCommandExecutor              INFO  Successfully connected to database.
All done, your SCM database is configured correctly!

```