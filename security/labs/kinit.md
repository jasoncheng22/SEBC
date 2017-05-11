```
[root@ip-172-31-43-176 ~]# kinit -V cloudera-scm@HADOOP.COM
Using default cache: /tmp/krb5cc_0
Using principal: cloudera-scm@HADOOP.COM
Password for cloudera-scm@HADOOP.COM:
Authenticated to Kerberos v5

```


```
[root@ip-172-31-43-176 ~]# klist
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: cloudera-scm@HADOOP.COM

Valid starting     Expires            Service principal
05/11/17 05:20:04  05/12/17 05:20:04  krbtgt/HADOOP.COM@HADOOP.COM
        renew until 05/18/17 05:20:04


```