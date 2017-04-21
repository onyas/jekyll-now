---
layout: post
title: Find the files that exactly matches the specified string
---

In linux environment,if we want to find which file contains the specified string,we can use the cmd as follows.



    1、grep "java" . -r -n
    
        find all the files included "java" in the current directory and subdirectories

    2、find ./ -name *.xml -exec grep -l "push-server" {} \;
    
        find all the xml file in the current directory and sub which contains "push-server"
