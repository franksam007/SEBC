### CM Install Lab
===
#### System Configuration Checks
---

1. Check vm.swappiness on nodes  
   ```# sysctl vm.swappiness```  
   >```vm.swappiness = 60```

   ```# sysctl -w vm.swappiness=1```   
   >```m.swappiness = 1```

2. The mount attributes of your volume(s)   
   ```# mount```   
   >```/dev/xvde on / type ext4 (rw)```   
   ```proc on /proc type proc (rw)```   
   ```sysfs on /sys type sysfs (rw)```
   ```devpts on /dev/pts type devpts (rw,gid=5,mode=620) ```  
   ```tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")```   
   ```none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)```

3. Reserve space setting  
   `#tune2fs -l /dev/xvde`  
>tune2fs 1.41.12 (17-May-2010)
Filesystem volume name:   centos_root  
Last mounted on:          /  
Filesystem UUID:          44d27f92-d3df-4207-80ea-22830afccf03  
Filesystem magic number:  0xEF53  
Filesystem revision #:    1 (dynamic)  
Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize  
Filesystem flags:         signed_directory_hash 
Default mount options:    (none)  
Filesystem state:         clean  
Errors behavior:          Continue  
Filesystem OS type:       Linux  
Inode count:              1966080  
Block count:              7864320  
Reserved block count:     393145  
Free blocks:              1897834  
Free inodes:              509073  
First block:              0  
Block size:               4096  
Fragment size:            4096   
Reserved GDT blocks:      510  
Blocks per group:         32768  
Fragments per group:      32768  
Inodes per group:         8192  
Inode blocks per group:   512  
Flex block group size:    16  
Filesystem created:       Tue Feb  4 23:38:21 2014  
Last mount time:          Mon May  8 07:39:07 2017  
Last write time:          Tue Feb  4 23:40:03 2014  
Mount count:              4  
Maximum mount count:      -1  
Last checked:             Tue Feb  4 23:38:21 2014  
Check interval:           0 (<none>)  
Lifetime writes:          819 MB   
Reserved blocks uid:      0 (user root)  
Reserved blocks gid:      0 (group root)  
First inode:              11  
Inode size:	          256  
Required extra isize:     28  
Desired extra isize:      28  
Journal inode:            8  
First orphan inode:       12201  
Default directory hash:   half_md4  
Directory Hash Seed:      21a3ffda-3d91-4393-b173-60a625eae109  
Journal backup:           inode blocks  


4. Disable transparent hugepage support  
   `# cat /sys/kernel/mm/transparent_hugepage/enabled`  
>cat: /sys/kernel/mm/transparent_hugepage/enabled: No such file or directory

5. List network interface configuration  
   ```# ifconfig```  
>```eth0      Link encap:Ethernet  HWaddr 06:F7:41:68:4A:18```      
          ```inet addr:172.31.44.106  Bcast:172.31.47.255  Mask:255.255.240.0```   
          ```inet6 addr: fe80::4f7:41ff:fe68:4a18/64 Scope:Link```
          ```UP BROADCAST RUNNING MULTICAST  MTU:9001  Metric:1```
          ```RX packets:1115 errors:0 dropped:0 overruns:0 frame:0```
          ```TX packets:1027 errors:0 dropped:0 overruns:0 carrier:0```
          ```collisions:0 txqueuelen:1000``` 
          ```RX bytes:70756 (69.0 KiB)  TX bytes:99901 (97.5 KiB)```
          ```Interrupt:24```
```lo        Link encap:Local Loopback```  
          ```inet addr:127.0.0.1  Mask:255.0.0.0```
          ```inet6 addr: ::1/128 Scope:Host```
          ```UP LOOPBACK RUNNING  MTU:16436  Metric:1```
          ```RX packets:0 errors:0 dropped:0 overruns:0 frame:0```
          ```TX packets:0 errors:0 dropped:0 overruns:0 carrier:0```
          ```collisions:0 txqueuelen:0 ```
6. Forward and reverse host lookups
   * `# getent hosts`  
>`127.0.0.1       localhost.localdomain localhost`
`127.0.0.1       localhost6.localdomain6 localhost6`
   * `# nslookup`  
   >`> ec2-35-162-167-87.us-west-2.compute.amazonaws.com`  
`Server:		172.31.0.2`  
`Address:	172.31.0.2#53`  
   `Non-authoritative answer:`  
`Name:	ec2-35-162-167-87.us-west-2.compute.amazonaws.com`  
`Address: 172.31.44.106`  
`> ec2-35-166-69-2.us-west-2.compute.amazonaws.com`  
`Server:		172.31.0.2`  
`Address:	172.31.0.2#53`  
`Non-authoritative answer:`  
`Name:	ec2-35-166-69-2.us-west-2.compute.amazonaws.com`  
`Address: 172.31.34.113`  
`> ec2-52-38-5-240.us-west-2.compute.amazonaws.com`  
`Server:		172.31.0.2`  
`Address:	172.31.0.2#53`  
`Non-authoritative answer:`  
`Name:	ec2-52-38-5-240.us-west-2.compute.amazonaws.com`  
`Address: 172.31.35.94`  
`> ec2-54-70-175-115.us-west-2.compute.amazonaws.com`  
`Server:		172.31.0.2`  
`Address:	172.31.0.2#53`  
`Non-authoritative answer:`  
`Name:	ec2-54-70-175-115.us-west-2.compute.amazonaws.com`  
`Address: 172.31.46.205`  
`> ec2-52-39-45-145.us-west-2.compute.amazonaws.com`  
`Server:		172.31.0.2`  
`Address:	172.31.0.2#53`  
`Non-authoritative answer:`  
`Name:	ec2-52-39-45-145.us-west-2.compute.amazonaws.com`  
`Address: 172.31.33.107`  
7.  `nscd` service status  
   `# service nscd start`  
>`Starting nscd:                                             [  OK  ]`  

`# service nscd status`  
>`nscd (pid 1409) is running...`   

8. `ntpd` service status  
   `service ntpd start`
  >`Starting ntpd:                                             [  OK  ]`   
  
`# service ntpd status`
  >`ntpd (pid  1499) is running...`      

