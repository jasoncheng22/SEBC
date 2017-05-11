5.9.2 to 5.10.1
```
[root@ip-172-31-45-227 ~]# curl -u jasoncheng22:cloudera http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/version
v15

[root@ip-172-31-45-227 ~]# curl -u jasoncheng22:cloudera http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v15/cm/version
{
  "version" : "5.10.1",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170319-2001",
  "gitHash" : "f226435f6fa5f545543c00245900ae43bea7a29c",
  "snapshot" : false
}


[root@ip-172-31-45-227 ~]# curl -u jasoncheng22:cloudera http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v15/users
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "jasoncheng22",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  } ]
}

[root@ip-172-31-45-227 ~]# curl -u jasoncheng22:cloudera http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v15/cm/scmDbInfo
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
```