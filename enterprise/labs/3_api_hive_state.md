## Check Hive Status
<code>
[root@ip-172-31-50-198 home]# curl -u FerrariLin:xup6m454   'http://52.71.91.38:7180/api/v18/clusters/FerrariLin/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}[root@ip-172-31-50-198 home]#  
</code>

## Stop Hive Service
<code>
[root@ip-172-31-50-198 home]# curl -X POST -u FerrariLin:xup6m454   'http://52.71.91.38:7180/api/v18/clusters/FerrariLin/services/hive/commands/stop'
{
  "id" : 257,
  "name" : "Stop",
  "startTime" : "2018-05-16T16:43:45.251Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@ip-172-31-50-198 home]# curl u FerrariLin:xup6m454   'http://52.71.91.38:7180/api/v18/clusters/FerrariLin/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STOPPED",
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
  "entityStatus" : "STOPPED"
}[root@ip-172-31-50-198 home]#
</code>

## Start Hive Service
<code>
[root@ip-172-31-50-198 home]# curl -X POST -u FerrariLin:xup6m454   'http://52.71.91.38:7180/api/v18/clusters/FerrariLin/services/hive/commands/start'
{
  "id" : 262,
  "name" : "Start",
  "startTime" : "2018-05-16T16:45:10.206Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
}[root@ip-172-31-50-198 home]# curl u FerrariLin:xup6m454   'http://52.71.91.38:7180/api/v18/clusters/FerrariLin/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTING",
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
  "entityStatus" : "STARTING"
}[root@ip-172-31-50-198 home]# curl -u FerrariLin:xup6m454   'http://52.71.91.38:7180/api/v18/clusters/FerrariLin/services/hive'
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive",
  "roleInstancesUrl" : "http://ip-172-31-49-64.ec2.internal:7180/cmf/serviceRedirect/hive/instances",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD",
    "suppressed" : false
  } ],
  "configStalenessStatus" : "FRESH",
  "clientConfigStalenessStatus" : "FRESH",
  "maintenanceMode" : false,
  "maintenanceOwners" : [ ],
  "displayName" : "Hive",
  "entityStatus" : "GOOD_HEALTH"
}[root@ip-172-31-50-198 home]#
</code>
