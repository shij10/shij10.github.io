---
title: how to install cassandra-driver
id: 58
categories:
  - Database
date: 2016-04-06 01:03:36
tags: [cassandra, python]
---

**Case:**

Istall cassandra-driver:   pip install cassandra-driver

Environment:

python 3.4.4rc1,  visual studio 2015 and VC++ common tools installed

**Issue:**

Microsoft Visual C++ 10.0 is required (Unable to find vcvarsall.bat)

**Fix:**

step 1, set VS100COMNTOOLS=%VS140COMNTOOLS%

step 2, copy vcvarsal.bat from /Microsoft Visual Studio 12.0/VC to /Microsoft Visual Studio 12.0/Common7/Tools/