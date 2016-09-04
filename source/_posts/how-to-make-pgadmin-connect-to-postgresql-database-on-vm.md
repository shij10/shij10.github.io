---
title: How to make pgAdmin connected to  postgresql database on VM?
id: 52
categories:
  - Database
date: 2016-03-01 16:59:42
tags: [pgAdmin, postgresql]
---

1. Install postgresql (e.g. centos: yum install postgresql-server).

2. Allow TCP/IP socket (suppose we're using PostgreSQL versio8.x or newer)
`  vi /var/lib/pgsql/data/postgresql.conf`
Find configuration line:
`  listen_addresses='localhost'`
And change it to:
`  listen_addresses='*'`
or
`  listen_addresses='x.x.x.x x.x.x.x'`

3. Enable client authentication
`  vi /var/lib/pgsql/data/pg_hba.conf`
and add the line":
`  host all all 10.10.29.0/24 trust`

4. restart PostgreSQL server
`  /etc/init.d/postgresql restart`
or
`  service postgresql restart`

5. Make port mapping. (e.g. 127.0.0.1:5432 -&gt; 10.0.2.15:5432)