<pre><code>{  
  "timestamp" : "2017-05-10T03:24:09.727Z",
  "clusters" : [ {
    "name" : "Cluster 1",
    "version" : "CDH5",
    "services" : [ {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "592445440"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-6ed3f599d1728b950ba031b5162bd81b",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-04e74ba5dd32c29c3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "21ahpawejo5z1l5ny877ha7f1"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-bf308ae72a03b299f7b2ba41a66a5bf7",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "5ca8ab5e-8ba3-4a66-8d1c-61f177015908"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1tkrudm45dxtepq8f9srw7ci1"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9pbkly7w68uje4erc0v3ax668"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "915406848"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3170683699"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400"
          }, {
            "name" : "rm_io_weight",
            "value" : "200"
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
          "value" : "8yjErG5ppyw3gNLZFiAejL2cWiUf4n"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "AZyktHeEn47SuGm2DM8ftMh6PvNCES"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "1eGdnnj7fWIitIATIqsicqQyMN0UAA"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-2a47c2fd497ff56f3f3b7c94f1296819",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "62261dc2-4cf7-4a3a-a74b-dadac210f29b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "91ddjl34oxffxrbdf75sjudpr"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-6ed3f599d1728b950ba031b5162bd81b",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-04e74ba5dd32c29c3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "bcy4z7vkia0pgmfbq75zowp1x"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-bf308ae72a03b299f7b2ba41a66a5bf7",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "5ca8ab5e-8ba3-4a66-8d1c-61f177015908"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "95pq4iik9nrex04s494wmd9pz"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-dd560b86b2481f3e799b3b2eaffd0a08",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dz1g8oo45dwl2gdnvwa5ebpo6"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ejna3ex57bno3jdgrzoodqd7"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-dd560b86b2481f3e799b3b2eaffd0a08",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cb9lvyax1oawmpqd7y375utg7"
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-dd560b86b2481f3e799b3b2eaffd0a08",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6au0qnli9d8pj5i4zp4pkeod"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-2a47c2fd497ff56f3f3b7c94f1296819",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "62261dc2-4cf7-4a3a-a74b-dadac210f29b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a56c2q5itkx0mcqnlwdnq78x3"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-6ed3f599d1728b950ba031b5162bd81b",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-04e74ba5dd32c29c3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2nkm7ivy0gzt5hntc9tcjple9"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-bf308ae72a03b299f7b2ba41a66a5bf7",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "5ca8ab5e-8ba3-4a66-8d1c-61f177015908"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ez2vnyyasz2ng1nhsmgodyf8"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice2"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice2"
          }, {
            "name" : "namenode_id",
            "value" : "101"
          }, {
            "name" : "role_jceks_password",
            "value" : "4yqp67bpp4vxx7c25dv874quw"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-dd560b86b2481f3e799b3b2eaffd0a08",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice2"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice2"
          }, {
            "name" : "namenode_id",
            "value" : "119"
          }, {
            "name" : "role_jceks_password",
            "value" : "amz3bwyuvasnwo5ymll2pjq8l"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-2a47c2fd497ff56f3f3b7c94f1296819",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "62261dc2-4cf7-4a3a-a74b-dadac210f29b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ddibx2sr3ak9v64r4kfvu2gj0"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-6ed3f599d1728b950ba031b5162bd81b",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "i-04e74ba5dd32c29c3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6sw0tza2h9dytosmr4tp42j2k"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-bf308ae72a03b299f7b2ba41a66a5bf7",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "5ca8ab5e-8ba3-4a66-8d1c-61f177015908"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "atuqzmjxcavl5h5hkb94qsi45"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7mlq683rhpg2dfb8dap180kvx"
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-dd560b86b2481f3e799b3b2eaffd0a08",
        "type" : "NFSGATEWAY",
        "hostRef" : {
          "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cxi5nd48twoj47j42amqgw79v"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "2"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "52428800"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600"
          }, {
            "name" : "rm_io_weight",
            "value" : "800"
          }, {
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
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3517"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "52428800"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3517"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "N56v7sKodnOuOKFmQcB0dNmq1KZcga"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e7lbzx6gjdbc55e2eokop7zd"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-2a47c2fd497ff56f3f3b7c94f1296819",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "62261dc2-4cf7-4a3a-a74b-dadac210f29b"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3l9gomyaqwuk6pzy799rcvjca"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-6ed3f599d1728b950ba031b5162bd81b",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-04e74ba5dd32c29c3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "a69qgamv0fmy20xqt2pnf0i6u"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-bf308ae72a03b299f7b2ba41a66a5bf7",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "5ca8ab5e-8ba3-4a66-8d1c-61f177015908"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9bfnvnvh97th0fsl7ha631w65"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-dd560b86b2481f3e799b3b2eaffd0a08",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2owrs3fl8tugcxqyti4iyl3o9"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "118"
          }, {
            "name" : "role_jceks_password",
            "value" : "9nqmjh6395mgzn7ujh64v52yz"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "191889408"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "191889408"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2602565632"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "438"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-44-106.us-west-2.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "123456"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-2a47c2fd497ff56f3f3b7c94f1296819",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "62261dc2-4cf7-4a3a-a74b-dadac210f29b"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-6ed3f599d1728b950ba031b5162bd81b",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-04e74ba5dd32c29c3"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-bf308ae72a03b299f7b2ba41a66a5bf7",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "5ca8ab5e-8ba3-4a66-8d1c-61f177015908"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-dd560b86b2481f3e799b3b2eaffd0a08",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6e2033noqzbzkqv07c6jofds3"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4hldik766zw5r2b5nkev0l5w3"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-44-106.us-west-2.compute.internal"
          }, {
            "name" : "oozie_database_name",
            "value" : "hue"
          }, {
            "name" : "oozie_database_password",
            "value" : "123456"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "hue"
          }, {
            "name" : "oozie_java_heapsize",
            "value" : "52428800"
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
        "name" : "oozie-OOZIE_SERVER-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b7tua73cq1vdf3v7j13eozwg5"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-44-106.us-west-2.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "123456"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-dd560b86b2481f3e799b3b2eaffd0a08"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-c7bc59f3f995d4a5d42569e2c9a5bb00",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "wut0dirx4114fyxssg18ous0"
          }, {
            "name" : "secret_key",
            "value" : "xUhP9xlQtl5d7VX5YTXzICvBsYeuQA"
          } ]
        }
      } ],
      "displayName" : "Hue"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761",
    "ipAddress" : "172.31.33.107",
    "hostname" : "ip-172-31-33-107.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "62261dc2-4cf7-4a3a-a74b-dadac210f29b",
    "ipAddress" : "172.31.34.113",
    "hostname" : "ip-172-31-34-113.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "5ca8ab5e-8ba3-4a66-8d1c-61f177015908",
    "ipAddress" : "172.31.35.94",
    "hostname" : "ip-172-31-35-94.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-04e74ba5dd32c29c3",
    "ipAddress" : "172.31.44.106",
    "hostname" : "ip-172-31-44-106.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "d83b0231-9d24-46d2-8bcd-74f0bc543a7f",
    "ipAddress" : "172.31.46.205",
    "hostname" : "ip-172-31-46-205.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-2a47c2fd497ff56f3f3b7c94f1296819",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "9904b475171e1332bc4a08300c650c03c83c48e1a04fd11297bff9656ade7ed0",
    "pwSalt" : -8877149738568912712,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-c7bc59f3f995d4a5d42569e2c9a5bb00",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5119590291fcb460b4b2ba0b309f536264adf1ef69ee938176032412a5e14d2d",
    "pwSalt" : 6058354408858471046,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-c7bc59f3f995d4a5d42569e2c9a5bb00",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "24ffad365de7dec0c8bfc75f2ecad1c155ae153ee724022dea2a65a5f384b3f8",
    "pwSalt" : 5449845343710914698,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-c7bc59f3f995d4a5d42569e2c9a5bb00",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b8ad89b650f23656c473dd77e4e4f708c0f4212c2c3658fed56a6a0eefba33ed",
    "pwSalt" : 6473398101322020067,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-c7bc59f3f995d4a5d42569e2c9a5bb00",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "5e194f18684c1854d4ed3b24d447caa83e4647e04a8c587d8a0ac471073f295d",
    "pwSalt" : -8951571994403813864,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "3107ff0443ada6d1b5675175cd91b89bfeeae895cd48615fd6d1daac308721a5",
    "pwSalt" : 6447346539638868167,
    "pwLogin" : true
  }, {
    "name" : "franksam007",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "9a61375feffb39dc3f644b9e85e0625ab3cd5e4476e3655225f9be0b4ebabeec",
    "pwSalt" : -5971508973793036544,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "b75d6918140bcdb4f6a54c7730c2a1faf8666e60823dfe36d95ff3da3f4c4498",
    "pwSalt" : -6389897587645754963,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.9.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170112-1158",
    "gitHash" : "a66d8bbdbe8bc3ee54235e55423f2f76c7d9f3b1",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-44-106.us-west-2.compute.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "123456"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        } ]
      }, {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "592445440"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-44-106.us-west-2.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "123456"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "592445440"
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
      "name" : "mgmt-ACTIVITYMONITOR-2a47c2fd497ff56f3f3b7c94f1296819",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "62261dc2-4cf7-4a3a-a74b-dadac210f29b"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "a05m9dalscq8p9yohyhe33irm"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-c7bc59f3f995d4a5d42569e2c9a5bb00",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "43zw621g7p7ea66gb746n6z4u"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-c7bc59f3f995d4a5d42569e2c9a5bb00",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "f33yhf0d8cta3276v1k5yycdg"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-c7bc59f3f995d4a5d42569e2c9a5bb00",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7ozfl8oygzgurjak9wmexdcbn"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-c7bc59f3f995d4a5d42569e2c9a5bb00",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "f4m0u4mi6pntet2iv43hh4biq"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-c7bc59f3f995d4a5d42569e2c9a5bb00",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "3fefb736-23a5-4713-b6bf-446d82a01761"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "41j85hz6l7mz6pryqkq9novuh"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 6:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://ec2-35-162-167-87.us-west-2.compute.amazonaws.com/cdh5.9.1/,http://archive.cloudera.com/cdh5/parcels/latest/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/"
    } ]
  }
}
</code></pre>