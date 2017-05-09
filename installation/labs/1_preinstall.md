# CM Install Lab
# System Configuration Checks

1. Check vm.swappiness on all your nodes
Set the value to 1 if necessary
```
[root@ip-172-31-37-250 ~]# echo 1 > /proc/sys/vm/swappiness

[root@ip-172-31-37-250 ~]# cat /proc/sys/vm/swappiness
1
[root@ip-172-31-37-250 ~]# vi /etc/sysctl.conf  
  > add vm.swappiness = 1 at the end of file.  
  > write & save & quit  
```

2. Show the mount attributes of your volume(s)
```
[root@ip-172-31-37-250 ~]# mount
/dev/xvde on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
```

3. If you have ext-based volumes, list the reserve space setting 
- XFS volumes do not support reserve space
```
[root@ip-172-31-40-159 ~]# resize2fs /dev/xvde
```

4. Disable transparent hugepage support
```
[root@ip-172-31-40-159 ~]# vi /etc/grub.conf
```

```
kernel /boot/vmlinuz-2.6.32-431.el6.x86_64 root=LABEL=centos_root ro transparent_hugepage=never
```

5. List your network interface configuration
```
[root@ip-172-31-40-159 ~]# ifconfig
eth0      Link encap:Ethernet  HWaddr 06:BC:60:F0:DD:2C
          inet addr:172.31.40.159  Bcast:172.31.47.255  Mask:255.255.240.0
          inet6 addr: fe80::4bc:60ff:fef0:dd2c/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1
          RX packets:20666 errors:0 dropped:0 overruns:0 frame:0
          TX packets:5057 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:27268378 (26.0 MiB)  TX bytes:463172 (452.3 KiB)
          Interrupt:24

lo        Link encap:Local Loopback
          inet addr:127.0.0.1  Mask:255.0.0.0
          inet6 addr: ::1/128 Scope:Host
          UP LOOPBACK RUNNING  MTU:16436  Metric:1
          RX packets:0 errors:0 dropped:0 overruns:0 frame:0
          TX packets:0 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:0
          RX bytes:0 (0.0 b)  TX bytes:0 (0.0 b)

```

6. Show that forward and reverse host lookups are correctly resolved

For /etc/hosts, use getent
```
[root@ip-172-31-35-111 ~]# getent hosts ec2-35-163-0-231.us-west-2.compute.amazonaws.com
172.31.45.227   ec2-35-163-0-231.us-west-2.compute.amazonaws.com
[root@ip-172-31-35-111 ~]# getent hosts ec2-52-33-168-91.us-west-2.compute.amazonaws.com
172.31.43.176   ec2-52-33-168-91.us-west-2.compute.amazonaws.com
[root@ip-172-31-35-111 ~]# getent hosts ec2-52-34-141-210.us-west-2.compute.amazonaws.com
172.31.41.138   ec2-52-34-141-210.us-west-2.compute.amazonaws.com
[root@ip-172-31-35-111 ~]# getent hosts ec2-34-210-93-122.us-west-2.compute.amazonaws.com
172.31.36.117   ec2-34-210-93-122.us-west-2.compute.amazonaws.com
[root@ip-172-31-35-111 ~]# getent hosts ec2-35-162-103-130.us-west-2.compute.amazonaws.com
172.31.35.111   ec2-35-162-103-130.us-west-2.compute.amazonaws.com
```

For DNS, use nslookup
```
yum install bind-utils -y

[root@ip-172-31-37-250 ~]# nslookup localhost
Server:         172.31.0.2
Address:        172.31.0.2#53

Name:   localhost
Address: 127.0.0.1

```

Show the nscd service is running
```
[root@ip-172-31-40-159 ~]# yum install nscd -y
[root@ip-172-31-40-159 ~]# service nscd start
Starting nscd:                                             [  OK  ]
[root@ip-172-31-40-159 ~]# service nscd status
nscd (pid 4480) is running...
```


Show the ntpd service is running
```
[root@ip-172-31-40-159 ~]# yum install ntp -y
[root@ip-172-31-40-159 ~]# service ntpd status
ntpd is stopped
[root@ip-172-31-40-159 ~]# service ntpd start
Starting ntpd:                                             [  OK  ]
[root@ip-172-31-40-159 ~]# service ntpd status
ntpd (pid  7624) is running...
```
