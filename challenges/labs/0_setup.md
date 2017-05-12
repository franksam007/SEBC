* Cloud Provider: AWS
* Node Name and IPs
  * ip-172-31-42-0.us-west-2.compute.internal: 172.31.42.0
  * ip-172-31-47-72.us-west-2.compute.internal: 172.31.47.72
  * ip-172-31-47-234.us-west-2.compute.internal: 172.31.47.234
  * ip-172-31-32-25.us-west-2.compute.internal: 172.31.32.25
  * ip-172-31-40-91.us-west-2.compute.internal: 172.31.40.91
* Linux release: CentOS 6.5
* Disk capacity in each node with "`df -h`" command
  * 172.31.42.0
><pre>Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm</pre>
  * 172.31.47.72
><pre>Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm</pre>
  * 172.31.47.234
><pre>Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm</pre>
  * 172.31.32.25
><pre>Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm</pre>
  * 172.31.40.91
><pre>Filesystem      Size  Used Avail Use% Mounted on
/dev/xvde        30G  654M   28G   3% /
tmpfs           7.4G     0  7.4G   0% /dev/shm</pre>
* Output of "`yum repolist enabled`"  
> <pre>Loaded plugins: fastestmirror, presto
Loading mirror speeds from cached hostfile
 \* base: mirrors.xmission.com
 \* extras: mirrors.tummy.com
 \* updates: repo1.sea.innoscale.net
repo id                          repo name                                    status
base                             CentOS-6 - Base                              6,706
extras                           CentOS-6 - Extras                               64
updates                          CentOS-6 - Updates                             270
repolist: 7,040
</pre>
* List of `passwd` entries
  * `zhou:x:2800:2900::/home/zhou:/bin/bash
`
  * `chen:x:2900:2800::/home/chen:/bin/bash`
* List of `shadow` entries
  * `shanghai:x:2800:`
  * `beijing:x:2900:`
