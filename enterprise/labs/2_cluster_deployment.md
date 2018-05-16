<code>
{
  "timestamp" : "2018-05-16T16:29:33.448Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "FerrariLin",
    "version" : "CDH5",
    "fullVersion" : "5.13.2",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-50-33.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive",
          "sensitive" : true
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-580c6dfe337e2ab00b329af51da6c036",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "6d19c1ec-682c-47ad-bdf9-d7e2d42b813f"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-7304c803c13237e014765852183f38f5",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "af7b37f1-9b36-4cb4-927a-583a24f5d830"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-953c4c15ca7b1111e63619cde3668c5d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "698002e3-c745-4cfa-b4a1-c6cd509d729f"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-65e857f1145bd48cdfd06727c8df6da5",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6hu3giilcx2zgte01v28chos2",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-085c61b10a27d3e5c590dc33d239b424",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4xd47ho9zbbon1kj5rz1djiew",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-65e857f1145bd48cdfd06727c8df6da5",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8ds8xdpat15hlbcfha8sgwjz9",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-1"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "2286944256",
            "sensitive" : false
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "228694425",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-1",
        "displayName" : "HiveServer2 Group 1",
        "roleType" : "HIVESERVER2",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "2286944256",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "4160539852",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "700",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "608174080",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "4160539852",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "700",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-085c61b10a27d3e5c590dc33d239b424",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "45b6qaf6hxseqgizwn7972c4k",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "3",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-65e857f1145bd48cdfd06727c8df6da5",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e4x7ovzc3cgenl9re9hqw2qzy",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "1",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-953c4c15ca7b1111e63619cde3668c5d",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "698002e3-c745-4cfa-b4a1-c6cd509d729f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bettrdi6sg1voeivfu1lvnf1t",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "2",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "608174080",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-50-33.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "database_password",
          "value" : "hue",
          "sensitive" : true
        }, {
          "name" : "database_type",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-085c61b10a27d3e5c590dc33d239b424",
          "sensitive" : false
        }, {
          "name" : "oozie_service",
          "value" : "oozie",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-085c61b10a27d3e5c590dc33d239b424",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "58omozru3daravdewkwlbx4e3",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_LOAD_BALANCER-BASE"
        }
      }, {
        "name" : "hue-HUE_SERVER-65e857f1145bd48cdfd06727c8df6da5",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "0f4e0673-ecf8-43a0-bd72-c0cf1d09a7d6",
            "sensitive" : true
          }, {
            "name" : "role_jceks_password",
            "value" : "7reatoa5gg2wlhq6j2lo06o5j",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "MCZdOJJOK0546XQ4tyFPSfKg70V4Nm",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      } ],
      "displayName" : "Hue",
      "roleConfigGroups" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-BASE",
        "displayName" : "Load Balancer Default Group",
        "roleType" : "HUE_LOAD_BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-HUE_SERVER-BASE",
        "displayName" : "Hue Server Default Group",
        "roleType" : "HUE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-KT_RENEWER-BASE",
        "displayName" : "Kerberos Ticket Renewer Default Group",
        "roleType" : "KT_RENEWER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-65e857f1145bd48cdfd06727c8df6da5",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "12geqn4dblez1t4vy9nm17oe0",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-50-33.ec2.internal",
            "sensitive" : false
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie",
            "sensitive" : true
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql",
            "sensitive" : false
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "rm_dirty",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "50",
          "sensitive" : false
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "U7vouDCvKHyHPa87WogeF6CxHC06bE",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-085c61b10a27d3e5c590dc33d239b424",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3nzbrbvrxdu8repqdoh11jas9",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-580c6dfe337e2ab00b329af51da6c036",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "6d19c1ec-682c-47ad-bdf9-d7e2d42b813f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4jnbyybo5bm65xoo4wp0hq46y",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-7304c803c13237e014765852183f38f5",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "af7b37f1-9b36-4cb4-927a-583a24f5d830"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "28ga9pgfxrbc032p9wovcmfiu",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-953c4c15ca7b1111e63619cde3668c5d",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "698002e3-c745-4cfa-b4a1-c6cd509d729f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "accqtsdnhdmj5icf0ddcgzg18",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-085c61b10a27d3e5c590dc33d239b424",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "50",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "4k53tqhndcqb55g3cb7rh0jq8",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6",
            "sensitive" : false
          }, {
            "name" : "mapred_submit_replication",
            "value" : "3",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "608174080",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1",
        "displayName" : "NodeManager Group 1",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1000",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "500",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "2",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "4670",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1000",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "500",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "2",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5047",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "608174080",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5047",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "2",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "o5Yz8paaPlm5By4fzgeAezmpV6hqp8",
          "sensitive" : true
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "TUXqJGFjgg4wYpK6CzRb6JhqJ9kkSd",
          "sensitive" : true
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "CfwWoC1jPjzUCPBqcTYNaZlrn1rMQX",
          "sensitive" : true
        }, {
          "name" : "rm_dirty",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "50",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-65e857f1145bd48cdfd06727c8df6da5",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-580c6dfe337e2ab00b329af51da6c036",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "6d19c1ec-682c-47ad-bdf9-d7e2d42b813f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "11fsrkjvg8nxkzflfs4kg9qbx",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-7304c803c13237e014765852183f38f5",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "af7b37f1-9b36-4cb4-927a-583a24f5d830"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1t984pvj6i75d8u7e0rektjf6",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-953c4c15ca7b1111e63619cde3668c5d",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "698002e3-c745-4cfa-b4a1-c6cd509d729f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "axxa9xygy2xa5o9rgcxmim42m",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-085c61b10a27d3e5c590dc33d239b424",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "52",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "7skilzbul35k8iaoaaot0n307",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-65e857f1145bd48cdfd06727c8df6da5",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dm0r2k7k4n06226nqq1cac7wv",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-SECONDARYNAMENODE-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824",
            "sensitive" : false
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "5292163072",
            "sensitive" : false
          }, {
            "name" : "rm_cpu_shares",
            "value" : "1000",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "500",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022",
            "sensitive" : false
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "608174080",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn",
            "sensitive" : false
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "608174080",
            "sensitive" : false
          } ]
        }
      } ],
      "replicationSchedules" : [ ],
      "snapshotPolicies" : [ ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.13.2-1.cdh5.13.2.p0.3",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.13.2-1.cdh5.13.2.p0.3",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ],
    "uuid" : "be4d2435-c21b-4c57-8eef-596dc9a73101"
  } ],
  "hosts" : [ {
    "hostId" : "0002fd45-033a-474c-aab5-bdbc8676bd22",
    "ipAddress" : "172.31.49.64",
    "hostname" : "ip-172-31-49-64.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "698002e3-c745-4cfa-b4a1-c6cd509d729f",
    "ipAddress" : "172.31.50.198",
    "hostname" : "ip-172-31-50-198.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "af7b37f1-9b36-4cb4-927a-583a24f5d830",
    "ipAddress" : "172.31.50.210",
    "hostname" : "ip-172-31-50-210.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee",
    "ipAddress" : "172.31.50.33",
    "hostname" : "ip-172-31-50-33.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "6d19c1ec-682c-47ad-bdf9-d7e2d42b813f",
    "ipAddress" : "172.31.50.64",
    "hostname" : "ip-172-31-50-64.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "FerrariLin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "5d95d6ef3a5aaa2caff7bae279a0cf5d507ef5a66bd158d5c548d16bc2a0e164",
    "pwSalt" : -4354948565532253,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-65e857f1145bd48cdfd06727c8df6da5",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "66087c78890c5d8a2956bcfa5ff365b89c52347bc910c0227fada6ffc49f2909",
    "pwSalt" : -4671537004807730277,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-085c61b10a27d3e5c590dc33d239b424",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "46d550e5f9b2250d92ef58f7b63d9572ff1470053a78ba2b20b674f979da457f",
    "pwSalt" : -2218985087068856565,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-085c61b10a27d3e5c590dc33d239b424",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f5f5b485e7cd17e3838c04b8e68697ad644962b0b6cbf954e47b76f427bb62d8",
    "pwSalt" : 3655904676250411030,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-085c61b10a27d3e5c590dc33d239b424",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "c11e179e0f9c6790682d33fc887cb88f84aab3dc5d7fa309eacf3ed59e0bbc7b",
    "pwSalt" : -7660110872858115192,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-085c61b10a27d3e5c590dc33d239b424",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "172994d1662e0dd8331371165deed52cc1f50400794ae6036343ef109d615716",
    "pwSalt" : 6117827172509510650,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "925c6a37b896997689f442ec50db7cf70d97e12a2ffdadd09e7aaa188850d2a1",
    "pwSalt" : -2505696240345895641,
    "pwLogin" : true
  }, {
    "name" : "root",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "db6648b924562f7829b34159ff26e78acddeebdc371c8eceb275747fa4c58296",
    "pwSalt" : 8383407913063138788,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.13.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20180205-1144",
    "gitHash" : "caa35e134bfc8a112ad1f3cae7d80a2b1f30796f",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-085c61b10a27d3e5c590dc33d239b424",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "37nj31qhicojxx2kdad6yq0b7",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-085c61b10a27d3e5c590dc33d239b424",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "497oz1bg8b8mvux1ozn4fefvi",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-085c61b10a27d3e5c590dc33d239b424",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "86z65ezcpvd1a546dojn44mqy",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-085c61b10a27d3e5c590dc33d239b424",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8xruzq3pxt9o765k941lmbzcf",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-085c61b10a27d3e5c590dc33d239b424",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "f443cc70-9d09-4f19-99e6-75b4a460e1ee"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bfzg6s33e5njtnrsn3qgrvq7c",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-50-33.ec2.internal",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman",
          "sensitive" : true
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-TELEMETRYPUBLISHER-BASE",
      "displayName" : "Telemetry Publisher Default Group",
      "roleType" : "TELEMETRYPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 14:50",
      "sensitive" : false
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD",
      "sensitive" : false
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://172.31.50.33/cdh5/",
      "sensitive" : false
    } ]
  },
  "allHostsConfig" : {
    "items" : [ {
      "name" : "rm_enabled",
      "value" : "true",
      "sensitive" : false
    } ]
  },
  "peers" : [ ],
  "hostTemplates" : {
    "items" : [ ]
  }
}
</code>
