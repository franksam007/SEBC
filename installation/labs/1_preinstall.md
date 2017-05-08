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

4. Disable transparent hugepage support  
   ``````

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

