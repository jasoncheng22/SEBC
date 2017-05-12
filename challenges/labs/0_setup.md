## List the cloud provider you are using (AWS, GCE, Azure, other)
```
AWS
```

## List your instances by their IP address and DNS name
IP address
```
>node1
[root@ip-172-31-17-68 ~]# getent hosts ec2-34-210-112-23.us-west-2.compute.amazonaws.com
172.31.17.68    ec2-34-210-112-23.us-west-2.compute.amazonaws.com

>node2
[root@ip-172-31-17-68 ~]# getent hosts ec2-34-210-124-17.us-west-2.compute.amazonaws.com
172.31.30.195   ec2-34-210-124-17.us-west-2.compute.amazonaws.com


>node3
[root@ip-172-31-17-68 ~]# getent hosts ec2-34-210-141-207.us-west-2.compute.amazonaws.com
172.31.27.167   ec2-34-210-141-207.us-west-2.compute.amazonaws.com

>node4
[root@ip-172-31-17-68 ~]# getent hosts ec2-52-37-17-244.us-west-2.compute.amazonaws.com
172.31.28.202   ec2-52-37-17-244.us-west-2.compute.amazonaws.com


>node5
[root@ip-172-31-17-68 ~]# getent hosts ec2-54-148-55-12.us-west-2.compute.amazonaws.com
172.31.25.79    ec2-54-148-55-12.us-west-2.compute.amazonaws.com
```

DNS name
```
[root@ip-172-31-17-68 ~]# nslookup localhost
Server:         172.31.0.2
Address:        172.31.0.2#53

Name:   localhost
Address: 127.0.0.1

```

## List the Linux release you are using
```
[root@ip-172-31-17-68 ~]# cat /etc/centos-release
CentOS release 6.5 (Final)
```

## List the file system capacity for the first node
```
[root@ip-172-31-17-68 ~]# df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  691M   28G   3% /
tmpfs            15G     0   15G   0% /dev/shm
```



List the command and output for yum repolist enabled
```
[root@ip-172-31-17-68 ~]# yum repolist enabled
Loaded plugins: fastestmirror, presto
Determining fastest mirrors
 * base: mirror.chpc.utah.edu
 * extras: mirrors.unifiedlayer.com
 * updates: mirror.pac-12.org
repo id                                                                    repo name                                                                              status
base                                                                       CentOS-6 - Base                                                                        6,706
extras                                                                     CentOS-6 - Extras                                                                         64
updates                                                                    CentOS-6 - Updates                                                                       270
repolist: 7,040

```


## List the /etc/passwd entries for zhou and chen
```
[root@ip-172-31-17-68 ~]# cat /etc/passwd

zhou:x:2800:2902::/home/zhou:/bin/bash
chen:x:2900:2901::/home/chen:/bin/bash
```


## List the /etc/group entries for shanghai and beijing
```
[root@ip-172-31-17-68 ~]# cat /etc/group

shanghai:x:2901:chen
beijing:x:2902:zhou
```
