[root@ip-172-31-50-33 home]# cat /etc/krb5.conf
[logging]
 default = FILE:/var/log/krb5libs.log
 kdc = FILE:/var/log/krb5kdc.log
 admin_server = FILE:/var/log/kadmind.log

[libdefaults]
 default_realm = FerrariLin
 dns_lookup_realm = false
 dns_lookup_kdc = false
 ticket_lifetime = 24h
 renew_lifetime = 7d
 forwardable = true

[realms]
 FerrariLin = {
  kdc = 172.31.50.33
  admin_server = 172.31.50.33
 }

[domain_realm]
 .FerrariLin = FerrariLin
 FerrariLin = FerrariLin
[root@ip-172-31-50-33 home]#
