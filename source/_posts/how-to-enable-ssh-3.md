---
title: 'Ubuntu: How To Enable SSH'
id: 48
categories:
  - Linux
date: 2016-02-17 00:18:44
tags: [ssh, ubuntu] 
---


1.	install openssh-server
    `sudo apt-get install openssh-server`
2.	edit the configuration file and look for the Port 22 line and uncomment it by removing the preceding hash sign
    `sudo vi /etc/ssh/ssh_config`
3.	restart the SSH service
    `sudo service ssh restart`  or
    `sudo /etc/init.d/ssh restart`
