```
[root@ip-172-31-35-111 ~]# curl -u jasoncheng22:cloudera http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v14/clusters
{
  "items" : [ {
    "name" : "cluster",
    "displayName" : "jasoncheng22",
    "version" : "CDH5",
    "fullVersion" : "5.9.2",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "clusterUrl" : "http://ip-172-31-45-227.us-west-2.compute.internal:7180/cmf/clusterRedirect/cluster",
    "hostsUrl" : "http://ip-172-31-45-227.us-west-2.compute.internal:7180/cmf/clusterRedirect/cluster/hosts",
    "entityStatus" : "GOOD_HEALTH"
  } ]
}


[root@ip-172-31-35-111 ~]# curl -u jasoncheng22:cloudera -X POST  http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v14/clusters/jasoncheng22/services/hive/commands/stop
{
  "id" : 383,
  "name" : "Stop",
  "startTime" : "2017-05-10T04:27:06.292Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }

}

[root@ip-172-31-35-111 ~]# curl -u jasoncheng22:cloudera -X POST  http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v14/clusters/jasoncheng22/services/hve/commands/start
{
  "id" : 387,
  "name" : "Start",
  "startTime" : "2017-05-10T04:28:08.686Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}

[root@ip-172-31-35-111 ~]# curl -u jasoncheng22:cloudera http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v14/clusters/jasoncheng22/services/hive
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-45-227.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-45-227.us-west-2.compute.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "DISABLED",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "DISABLED",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "DISABLED_HEALTH"
}[
```


