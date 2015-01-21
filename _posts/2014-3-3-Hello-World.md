---
layout: post
title: How to find the script of a process in linux
---

1、ps -ef |grep XXXXX  
  get the PID
2、ll /proc/PID
  get the directory
  
  for example
  
-bash-3.2# ps -ef |grep zookeeper
root     12970     1  0  2014 ?        01:58:00 /usr/java/jdk1.6.0_45/bin/java -Dzookeeper.log.dir=. -Dzookeeper.root.logger=INFO,CONSOLE -cp /home/zookeeper-3.4.5/bin/../build/classes:/home/zookeeper-3.4.5/bin/../build/lib/*.jar:/home/zookeeper-3.4.5/bin/../lib/slf4j-log4j12-1.6.1.jar:/home/zookeeper-3.4.5/bin/../lib/slf4j-api-1.6.1.jar:/home/zookeeper-3.4.5/bin/../lib/netty-3.2.2.Final.jar:/home/zookeeper-3.4.5/bin/../lib/log4j-1.2.15.jar:/home/zookeeper-3.4.5/bin/../lib/jline-0.9.94.jar:/home/zookeeper-3.4.5/bin/../zookeeper-3.4.5.jar:/home/zookeeper-3.4.5/bin/../src/java/lib/*.jar:/home/zookeeper-3.4.5/bin/../conf: -Dcom.sun.management.jmxremote -Dcom.sun.management.jmxremote.local.only=false org.apache.zookeeper.server.quorum.QuorumPeerMain /home/zookeeper-3.4.5/bin/../conf/zoo.cfg
root     19336 19224  0 13:57 pts/1    00:00:00 grep zookeeper

-bash-3.2# ll /proc/12970
总计 0
dr-xr-xr-x  2 root root 0 01-21 13:57 attr
-r--------  1 root root 0 01-21 13:57 auxv
-r--r--r--  1 root root 0 01-20 10:58 cmdline
-rw-r--r--  1 root root 0 01-21 13:57 coredump_filter
-r--r--r--  1 root root 0 01-21 13:57 cpuset
lrwxrwxrwx  1 root root 0 01-21 13:57 cwd -> /home/zookeeper-3.4.5
-r--------  1 root root 0 01-21 13:57 environ
lrwxrwxrwx  1 root root 0 01-21 13:57 exe -> /usr/java/jdk1.6.0_45/bin/java
dr-x------  2 root root 0 01-21 13:57 fd
-r--r--r--  1 root root 0 01-21 13:57 io
-r--------  1 root root 0 01-21 13:57 limits
-rw-r--r--  1 root root 0 01-21 13:57 loginuid
-r--r--r--  1 root root 0 01-21 13:57 maps
-rw-------  1 root root 0 01-21 13:57 mem
-r--r--r--  1 root root 0 01-21 13:57 mounts
-r--------  1 root root 0 01-21 13:57 mountstats
-r--r--r--  1 root root 0 01-21 13:57 numa_maps
-rw-r--r--  1 root root 0 01-21 13:57 oom_adj
-r--r--r--  1 root root 0 01-21 13:57 oom_score
lrwxrwxrwx  1 root root 0 01-21 13:57 root -> /
-r--r--r--  1 root root 0 01-21 13:57 schedstat
-r--r--r--  1 root root 0 01-21 13:57 smaps
-r--r--r--  1 root root 0 01-20 10:58 stat
-r--r--r--  1 root root 0 01-21 13:57 statm
-r--r--r--  1 root root 0 01-20 10:58 status
dr-xr-xr-x 22 root root 0 01-21 13:57 task
-r--r--r--  1 root root 0 01-21 13:57 wchan
