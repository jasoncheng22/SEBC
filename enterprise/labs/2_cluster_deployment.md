Browse or use curl on the endpoint ./api/v2/cm/deployment
```
[root@ip-172-31-35-111 ~]# curl -X GET -u "jasoncheng22:cloudera" -i http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v2/cm/deployment
HTTP/1.1 200 OK
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=1j4xuq3d167f013uwx9u9cpxib;Path=/;HttpOnly
Content-Type: application/json
Date: Wed, 10 May 2017 03:26:00 GMT
Transfer-Encoding: chunked
Server: Jetty(6.1.26.cloudera.4)

{
  "timestamp" : "2017-05-10T03:26:00.865Z",
  "clusters" : [ {
    "name" : "jasoncheng22",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "440401920"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "440401920"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "912680550"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "153"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-45-227.us-west-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "password"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-0f4a424435ce7ecf0c653746e9eb23eb",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-031d137485c1734f3"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-6007b21aee16913b162cff7349be14eb",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-a3e5491574b89b1d4dffb32d6ce0e75f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-012dda69adee56be7"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-e6119a5544c26848e583a1427270d251",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-085e766a393f7509f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dk2xlfrv6gjykp4oms7r2c15c"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9mpyi7lqxht3a4xeljbzg3epw"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "440401920"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "efw8sgrj8r2p1ldktdi51tu2d"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-6007b21aee16913b162cff7349be14eb",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1jxohhdkxxwb9j5wiu0p4qwdz"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-e6119a5544c26848e583a1427270d251",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-085e766a393f7509f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ed2rmksc51k7z6oji5dvctlx6"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-45-227.us-west-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "password"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-6007b21aee16913b162cff7349be14eb"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "etcghkt6xbojxorh854glte71"
          }, {
            "name" : "secret_key",
            "value" : "y3QmF71gpManXbLUWpuDPWEZq98iDw"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-45-227.us-west-2.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "password"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "440401920"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7rf3mr1fpt5hrcgnd1vjc6q8m"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "10"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "440401920"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5250"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5250"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "3wbOIyxUQO3SKKWJ2pk0VLkStuW5V5"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5nyp8qo9iha49bp7531yn6hd0"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-0f4a424435ce7ecf0c653746e9eb23eb",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-031d137485c1734f3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e1c5ulprzcig26xn6wozcvbn2"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "43r06wr14cpc1ggm9p10qlcnt"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-6007b21aee16913b162cff7349be14eb",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b0beyf0ouis4iztt6qymw5agq"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-a3e5491574b89b1d4dffb32d6ce0e75f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-012dda69adee56be7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1ga1xinbny1wl1mb4bezt1bvv"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-e6119a5544c26848e583a1427270d251",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-085e766a393f7509f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4gsh4h6ng17grpbywa4rd3epx"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-6007b21aee16913b162cff7349be14eb",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "94"
          }, {
            "name" : "role_jceks_password",
            "value" : "brdggr6yhlpad6tjk7acfl4kr"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "440401920"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_handler_count",
            "value" : "32"
          }, {
            "name" : "dfs_namenode_service_handler_count",
            "value" : "32"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "1073741824"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "1073741824"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "Mll4tztBozLdGthlFuomq1NVK33nyB"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "RWI5rADmgjq1YK7M1VcgDaELYbL1ux"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "Iilwkk32DVEH44YsgyZiw3gzlPoimd"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-0f4a424435ce7ecf0c653746e9eb23eb",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-031d137485c1734f3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "clpu71y1dodlj1k8qejwuv5ss"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3hl08pnm8ju83dnw8t363jv4b"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-6007b21aee16913b162cff7349be14eb",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5kr7jwdqq2pjvgebyrsxcn1u3"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-a3e5491574b89b1d4dffb32d6ce0e75f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-012dda69adee56be7"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2rev82d4s2bvhktq1n9m0tsej"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-e6119a5544c26848e583a1427270d251",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-085e766a393f7509f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4cc1jrdjw71gag3s89g7tco3r"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5sv1f49srpofsn6ttorvh3gvn"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-6007b21aee16913b162cff7349be14eb",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5mkmin6jegqotr782bphe8cq5"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b4x4fts4f1lou7x5o51fi0vkn"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-6007b21aee16913b162cff7349be14eb",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "em6gpjtpy5k8ylkpsuguke8zg"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-e6119a5544c26848e583a1427270d251",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-085e766a393f7509f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "amie7qvli35wimsf6svb6zyso"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-5e07558629ca2a07b81ffdbd6a1c0039",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0e88a545db56e1c28"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "103"
          }, {
            "name" : "role_jceks_password",
            "value" : "cw1tu15iej8sgk0o529tgcmii"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-6007b21aee16913b162cff7349be14eb",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0b09e6f7ea6cfb441"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "96"
          }, {
            "name" : "role_jceks_password",
            "value" : "7nuk45vinrnwepjvzbkympam3"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "i-0e88a545db56e1c28",
    "ipAddress" : "172.31.35.111",
    "hostname" : "ip-172-31-35-111.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0b09e6f7ea6cfb441",
    "ipAddress" : "172.31.36.117",
    "hostname" : "ip-172-31-36-117.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-085e766a393f7509f",
    "ipAddress" : "172.31.41.138",
    "hostname" : "ip-172-31-41-138.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-031d137485c1734f3",
    "ipAddress" : "172.31.43.176",
    "hostname" : "ip-172-31-43-176.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-012dda69adee56be7",
    "ipAddress" : "172.31.45.227",
    "hostname" : "ip-172-31-45-227.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-5e07558629ca2a07b81ffdbd6a1c0039",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "dc27e524666362eb78b027e975cc0feb36456ea108ba8df8263b22d47a7e1678",
    "pwSalt" : -1401817446354464339,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-5e07558629ca2a07b81ffdbd6a1c0039",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "dfc336c891cba3d5a75b989cbf689d4188e5daa9ec9b170114ac36c576b6d18b",
    "pwSalt" : -939353982198291526,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATOR-5e07558629ca2a07b81ffdbd6a1c0039",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "2b92c5bd780c8e8a489d8683b17ef9f9b188e71904d2ba99b699dcf8284a9496",
    "pwSalt" : -584341896143157682,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-NAVIGATORMETASERVER-5e07558629ca2a07b81ffdbd6a1c0039",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "40e133d4e9503dbecfe80d85b5332e886ac255f141dd05cc00965d988667eb84",
    "pwSalt" : 8627357206782082489,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-5e07558629ca2a07b81ffdbd6a1c0039",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "ab7761a7d6da1019bc144a978cf8ea464a1801a8298bf802b70974d0d74760e8",
    "pwSalt" : -2644228854974004644,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-5e07558629ca2a07b81ffdbd6a1c0039",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f9f0e553190838efbb4c2e76e90387a4c71fb7c32be97c704f8156d7de328483",
    "pwSalt" : -6550122397933900584,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "668b913cdb1844ef0519c3b3be880d5a1f1b6e8fd63be837d390fed3cb46ecdf",
    "pwSalt" : 2621878240026416538,
    "pwLogin" : true
  }, {
    "name" : "jasoncheng22",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "c6e372fc5f1fa57d2811334907f77d1050f70fefdc45d1919f747405b845d6be",
    "pwSalt" : 5460316901485072581,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "2a889fd67f5d8a459f1fb668782502505c74824bcacffb5d91544589d3471425",
    "pwSalt" : 9170757652653745119,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170330-1814",
    "gitHash" : "822da28bff818f57fc1bfc3eafe3a550300ef1b0",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "440401920"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "NAVIGATOR",
        "items" : [ {
          "name" : "navigator_database_host",
          "value" : "ip-172-31-45-227.us-west-2.compute.internal"
        }, {
          "name" : "navigator_database_password",
          "value" : "password"
        }, {
          "name" : "navigator_heapsize",
          "value" : "440401920"
        } ]
      }, {
        "roleType" : "NAVIGATORMETASERVER",
        "items" : [ {
          "name" : "nav_metaserver_database_host",
          "value" : "ip-172-31-45-227.us-west-2.compute.internal"
        }, {
          "name" : "nav_metaserver_database_password",
          "value" : "password"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-45-227.us-west-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "password"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "440401920"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-5e07558629ca2a07b81ffdbd6a1c0039",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-0e88a545db56e1c28"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "aehrwx6bw47xphuwntao25765"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-5e07558629ca2a07b81ffdbd6a1c0039",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-0e88a545db56e1c28"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bkb8jyeaaztn7e769frqwnrc5"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-5e07558629ca2a07b81ffdbd6a1c0039",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-0e88a545db56e1c28"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "f3h3djoly2wqhsjrije4i07gf"
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-5e07558629ca2a07b81ffdbd6a1c0039",
      "type" : "NAVIGATOR",
      "hostRef" : {
        "hostId" : "i-0e88a545db56e1c28"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "e2ii1940quug4x8ge20dksq2l"
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-5e07558629ca2a07b81ffdbd6a1c0039",
      "type" : "NAVIGATORMETASERVER",
      "hostRef" : {
        "hostId" : "i-0e88a545db56e1c28"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "77gfftnrqkkvgtqsru09rejrj"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-5e07558629ca2a07b81ffdbd6a1c0039",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-0e88a545db56e1c28"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2p6w5i6q8p5yy0e5hyz79u9rn"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-5e07558629ca2a07b81ffdbd6a1c0039",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-0e88a545db56e1c28"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7kmhtitm1j6qhhvzjs58sqewy"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 5:10"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}[root@ip-172-31-35-111 ~]#



[root@ip-172-31-35-111 ~]# curl -X GET -u "minotaur:minotaur" -i http://ec2-35-163-0-231.us-west-2.compute.amazonaws.com:7180/api/v2/cm/deployment
HTTP/1.1 403 Forbidden
Expires: Thu, 01-Jan-1970 00:00:00 GMT
Set-Cookie: CLOUDERA_MANAGER_SESSIONID=5z8goy7ugnwb12haobl74i7i7;Path=/;HttpOnly
Content-Length: 0
Date: Wed, 10 May 2017 03:26:27 GMT
Server: Jetty(6.1.26.cloudera.4)

```
Store the output in enterprise/labs/2_cluster_deployment.md
Code-format this output for readability
