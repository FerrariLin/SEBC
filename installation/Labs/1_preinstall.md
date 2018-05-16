## <center>0.AWS-CreateInstance</p>
<center> <img src=Aws-instance-add-host.png> </center>
<center> <img src=Aws-instance-set-securityGroup.png> </center>
<center> <img src=Aws-instance-volume.png> </center>
<center> <img src=Aws-instance-set-ElasticIP.png> </center>

## <center>1.Check swappiness</p>
<code>
mn01
[root@ip-172-31-55-156 home]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-55-156 home]# 
mn02
[root@ip-172-31-63-54 home]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-63-54 home]#
wn01
[root@ip-172-31-55-193 home]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-55-193 home]#
wn02
[root@ip-172-31-53-126 ~]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-53-126 ~]#
wn03
[root@ip-172-31-49-68 ~]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-49-68 ~]#
</code>

## <center>2.Mount Attributes</p>
<code>
[root@ip-172-31-55-156 home]# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  200G  0 disk
`-xvda1 202:1    0  200G  0 part /
[root@ip-172-31-55-156 home]#
[root@ip-172-31-63-54 home]# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  200G  0 disk
`-xvda1 202:1    0  200G  0 part /
[root@ip-172-31-63-54 home]#
[root@ip-172-31-55-193 home]# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  200G  0 disk
`-xvda1 202:1    0  200G  0 part /
[root@ip-172-31-55-193 home]#
[root@ip-172-31-53-126 ~]# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  200G  0 disk
`-xvda1 202:1    0  200G  0 part /
[root@ip-172-31-53-126 ~]#
[root@ip-172-31-49-68 ~]# lsblk
NAME    MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
xvda    202:0    0  200G  0 disk
`-xvda1 202:1    0  200G  0 part /
[root@ip-172-31-49-68 ~]#
</code>
<center> <img src=Host-filesystem-001.png > </center>
<center> <img src=Host-filesystem-002.png > </center>
<center> <img src=Host-filesystem-003.png > </center>
<center> <img src=Host-filesystem-004.png > </center>
<center> <img src=Host-filesystem-005.png > </center>

## <center>3.Volume Type</p>
[root@ip-172-31-55-156 home]# file -sL /dev/xvda1
/dev/xvda1: Linux rev 1.0 ext4 filesystem data (needs journal recovery) (extents) (large files) (huge files)
[root@ip-172-31-55-156 home]#

[root@ip-172-31-63-54 home]# file -sL /dev/xvda1
/dev/xvda1: Linux rev 1.0 ext4 filesystem data (needs journal recovery) (extents) (large files) (huge files)
[root@ip-172-31-63-54 home]#

[root@ip-172-31-55-193 home]# file -sL /dev/xvda1
/dev/xvda1: Linux rev 1.0 ext4 filesystem data (needs journal recovery) (extents) (large files) (huge files)
[root@ip-172-31-55-193 home]#

[root@ip-172-31-53-126 ~]# file -sL /dev/xvda1
/dev/xvda1: Linux rev 1.0 ext4 filesystem data (needs journal recovery) (extents) (large files) (huge files)
[root@ip-172-31-53-126 ~]#

[root@ip-172-31-49-68 ~]# file -sL /dev/xvda1
/dev/xvda1: Linux rev 1.0 ext4 filesystem data (needs journal recovery) (extents) (large files) (huge files)
[root@ip-172-31-49-68 ~]#

## <center>4.Disable Hugepage</p>
<center> <img src=Set_hugepage.png> </center>

## <center>5.Network Interface Configuration</p>
<code>
 [root@ip-172-31-55-156 home]# ifconfig
eth0      Link encap:Ethernet  HWaddr 06:B7:6C:CA:A2:D4
          inet addr:172.31.55.156  Bcast:172.31.63.255  Mask:255.255.240.0
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:3901598 errors:0 dropped:0 overruns:0 frame:0
          TX packets:2783360 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:5428593669 (5.0 GiB)  TX bytes:7737990014 (7.2 GiB)
          Interrupt:145

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:58157 errors:0 dropped:0 overruns:0 frame:0
          TX packets:58157 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:1003422081 (956.9 MiB)  TX bytes:1003422081 (956.9 MiB)

[root@ip-172-31-55-156 home]# cat /etc/sysconfig/network-scripts/ifcfg-eth0
DEVICE="eth0"
BOOTPROTO="dhcp"
IPV6INIT="yes"
MTU="1500"
NM_CONTROLLED="yes"
ONBOOT="yes"
TYPE="Ethernet"
UUID="52658143-fe10-477a-861f-410a6e8f57e4"
[root@ip-172-31-55-156 home]#

[root@ip-172-31-63-54 home]# ifconfig
eth0      Link encap:Ethernet  HWaddr 06:09:65:94:06:0C
          inet addr:172.31.63.54  Bcast:172.31.63.255  Mask:255.255.240.0
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:2023393 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1617285 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:4689061921 (4.3 GiB)  TX bytes:7234728915 (6.7 GiB)
          Interrupt:145

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:157616 errors:0 dropped:0 overruns:0 frame:0
          TX packets:157616 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:944985557 (901.2 MiB)  TX bytes:944985557 (901.2 MiB)

[root@ip-172-31-63-54 home]# cat /etc/sysconfig/network-scripts/ifcfg-eth0
DEVICE="eth0"
BOOTPROTO="dhcp"
IPV6INIT="yes"
MTU="1500"
NM_CONTROLLED="yes"
ONBOOT="yes"
TYPE="Ethernet"
UUID="52658143-fe10-477a-861f-410a6e8f57e4"
[root@ip-172-31-63-54 home]#

[root@ip-172-31-55-193 home]# ifconfig
eth0      Link encap:Ethernet  HWaddr 06:2F:CC:2E:C9:F0
          inet addr:172.31.55.193  Bcast:172.31.63.255  Mask:255.255.240.0
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:1522673 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1145430 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:4922948725 (4.5 GiB)  TX bytes:1951757689 (1.8 GiB)
          Interrupt:145

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:17705 errors:0 dropped:0 overruns:0 frame:0
          TX packets:17705 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:35367164 (33.7 MiB)  TX bytes:35367164 (33.7 MiB)

[root@ip-172-31-55-193 home]# cat /etc/sysconfig/network-scripts/ifcfg-eth0
DEVICE="eth0"
BOOTPROTO="dhcp"
IPV6INIT="yes"
MTU="1500"
NM_CONTROLLED="yes"
ONBOOT="yes"
TYPE="Ethernet"
UUID="52658143-fe10-477a-861f-410a6e8f57e4"
[root@ip-172-31-55-193 home]#

[root@ip-172-31-53-126 ~]# ifconfig
eth0      Link encap:Ethernet  HWaddr 06:10:2B:4D:0F:C4
          inet addr:172.31.53.126  Bcast:172.31.63.255  Mask:255.255.240.0
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:1605411 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1133140 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:4926812109 (4.5 GiB)  TX bytes:1897711708 (1.7 GiB)
          Interrupt:145

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:18167 errors:0 dropped:0 overruns:0 frame:0
          TX packets:18167 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:35349713 (33.7 MiB)  TX bytes:35349713 (33.7 MiB)

[root@ip-172-31-53-126 ~]# cat /etc/sysconfig/network-scripts/ifcfg-eth0
DEVICE="eth0"
BOOTPROTO="dhcp"
IPV6INIT="yes"
MTU="1500"
NM_CONTROLLED="yes"
ONBOOT="yes"
TYPE="Ethernet"
UUID="52658143-fe10-477a-861f-410a6e8f57e4"
[root@ip-172-31-53-126 ~]#

[root@ip-172-31-49-68 ~]# ifconfig
eth0      Link encap:Ethernet  HWaddr 06:35:CB:26:18:F2
          inet addr:172.31.49.68  Bcast:172.31.63.255  Mask:255.255.240.0
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:1636184 errors:0 dropped:0 overruns:0 frame:0
          TX packets:1196405 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:4935107148 (4.5 GiB)  TX bytes:1899888469 (1.7 GiB)
          Interrupt:145

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          UP LOOPBACK RUNNING  MTU:65536  Metric:1
          RX packets:18621 errors:0 dropped:0 overruns:0 frame:0
          TX packets:18621 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:35919286 (34.2 MiB)  TX bytes:35919286 (34.2 MiB)

[root@ip-172-31-49-68 ~]# cat /etc/sysconfig/network-scripts/ifcfg-eth0
DEVICE="eth0"
BOOTPROTO="dhcp"
IPV6INIT="yes"
MTU="1500"
NM_CONTROLLED="yes"
ONBOOT="yes"
TYPE="Ethernet"
UUID="52658143-fe10-477a-861f-410a6e8f57e4"
[root@ip-172-31-49-68 ~]#
</code>

## <center>6.Getent&nslookup</p>
<code>
[root@ip-172-31-49-68 ~]# getent hosts
127.0.0.1       localhost localhost.localdomain localhost4 localhost4.localdomain4
172.31.55.156   ip-172-31-55-156.ec2.internal
172.31.63.54    ip-172-31-63-54.ec2.internal
172.31.55.193   ip-172-31-55-193.ec2.internal
172.31.53.126   ip-172-31-53-126.ec2.internal
172.31.49.68    ip-172-31-49-68.ec2.internal
[root@ip-172-31-49-68 ~]#
</code>

<code>
[root@ip-172-31-55-156 home]# nslookup 172.31.55.156
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
156.55.31.172.in-addr.arpa	name = ip-172-31-55-156.ec2.internal.

Authoritative answers can be found from:

[root@ip-172-31-55-156 home]#

[root@ip-172-31-63-54 home]# nslookup 172.31.63.54
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
54.63.31.172.in-addr.arpa	name = ip-172-31-63-54.ec2.internal.

Authoritative answers can be found from:

[root@ip-172-31-63-54 home]#

[root@ip-172-31-55-193 home]# nslookup 172.31.55.193
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
193.55.31.172.in-addr.arpa	name = ip-172-31-55-193.ec2.internal.

Authoritative answers can be found from:

[root@ip-172-31-55-193 home]#

[root@ip-172-31-53-126 ~]# nslookup 172.31.53.126
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
126.53.31.172.in-addr.arpa	name = ip-172-31-53-126.ec2.internal.

Authoritative answers can be found from:

[root@ip-172-31-53-126 ~]#

[root@ip-172-31-49-68 ~]# nslookup 172.31.49.68
Server:		172.31.0.2
Address:	172.31.0.2#53

Non-authoritative answer:
68.49.31.172.in-addr.arpa	name = ip-172-31-49-68.ec2.internal.

Authoritative answers can be found from:

[root@ip-172-31-49-68 ~]#
</code>

## <center>7.Run nscd</p>
<code>
[root@ip-172-31-55-156 home]# service nscd status
nscd (pid 16941) is running...
[root@ip-172-31-55-156 home]#
</code>

## <center>8.Run ntpd</p>
<code>
[root@ip-172-31-55-156 home]# service ntpd status
ntpd (pid  11765) is running...
[root@ip-172-31-55-156 home]#
</code>
<center> <img src=set_ntp.conf-server.png> </center>
<center> <img src=set_ntp.conf-otherhost.png> </center>
<center> <img src=ntpcheck-sever.png> </center>
<center> <img src=ntpcheck-otherhost.png> </center>


## <center>9.Disable SeLinex & FireWall</p>
<center> <img src=Disable_Selinux.png > </center>
<center> <img src=disable_iptables.png > </center>



