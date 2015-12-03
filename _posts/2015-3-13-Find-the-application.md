---
layout: post
title: How to find the application used the assigned port
---

usually,we want to find which application is using the assigned port,like 8080,here is the example.

    1、netstat -apn | grep 8080   or  netstat -ntulp | grep ':8419'
    
        get the pid or name

    2、ps -ef |grep pid or name
    
        get the application
