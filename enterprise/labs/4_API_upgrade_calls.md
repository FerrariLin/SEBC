## Report the latest available version of the API
<code>
[root@ip-172-31-50-198 yum.repos.d]# curl -u FerrariLin:xup6m454 'http://52.71.91.38:7180/api/version/'
v19
[root@ip-172-31-50-198 yum.repos.d]#
</code>

## Report the CM version
<code>
[root@ip-172-31-50-198 yum.repos.d]# curl -u FerrariLin:xup6m454 'http://52.71.91.38:7180/api/v19/cm/version'
{
  "version" : "5.14.2",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20180402-2155",
  "gitHash" : "4adcd280dde9c492680ada3ee369b4e97d22137a",
  "snapshot" : false
}[root@ip-172-31-50-198 yum.repos.d]#
</code>

## List all CM users
<code>
[root@ip-172-31-50-198 yum.repos.d]# curl -u FerrariLin:xup6m454 'http://52.71.91.38:7180/api/v19/users'
{
  "items" : [ {
    "name" : "FerrariLin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ]
  }, {
    "name" : "root",
    "roles" : [ "ROLE_ADMIN" ]
  } ]
}[root@ip-172-31-50-198 yum.repos.d]#
</code>

## Report the database server in use by CM
<code>
[root@ip-172-31-50-198 yum.repos.d]# curl -u FerrariLin:xup6m454 'http://52.71.91.38:7180/api/v19/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}[root@ip-172-31-50-198 yum.repos.d]#
</code>
