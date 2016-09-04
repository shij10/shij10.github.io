---
title: The step of setup django web
id: 33
categories:
  - web
date: 2016-01-07 00:34:24
tags: [django]
---


# start a project

$ django-admin.py startproject mysite

![](/img/onenote-568d41e22c3760.36676796.png)

# start a app

$ python manage.py startapp polls

![](/img/onenote-568d41e35443d7.31308359.png)

# modify ENGINE, NAME

<span style="font-family: Arial; font-size: 10pt; background-color: yellow;">from os import path</span>

<span style="font-family: Arial; font-size: 10pt; background-color: yellow;">PROJECT_ROOT = path.dirname(path.abspath(path.dirname(__file__)))</span>

<span style="font-family: Arial; font-size: 10pt;">DATABASES = {</span>

<span style="font-family: Arial; font-size: 10pt;"> 'default': {</span>

<span style="font-family: Arial; font-size: 10pt;"> 'ENGINE': 'django.db.backends</span><span style="font-family: Arial; font-size: 10pt; background-color: yellow;">.sqlite3</span><span style="font-family: Arial; font-size: 10pt;">', # Add 'postgresql_psycopg2', 'mysql', 'sqlite3' or 'oracle'.</span>

<span style="font-family: Arial; font-size: 10pt;"> 'NAME': </span><span style="font-family: Arial; font-size: 10pt; background-color: yellow;">path.join(PROJECT_ROOT, 'db.sqlite3')</span><span style="font-family: Arial; font-size: 10pt;">, # Or path to database file if using sqlite3.</span>

<span style="font-family: Arial; font-size: 10pt;"> 'USER': '', # Not used with sqlite3.</span>

<span style="font-family: Arial; font-size: 10pt;"> 'PASSWORD': '', # Not used with sqlite3.</span>

<span style="font-family: Arial; font-size: 10pt;"> 'HOST': '', # Set to empty string for localhost. Not used with sqlite3.</span>

<span style="font-family: Arial; font-size: 10pt;"> 'PORT': '', # Set to empty string for default. Not used with sqlite3.</span>

<span style="font-family: Arial; font-size: 10pt;"> }</span>

<span style="font-family: Arial; font-size: 10pt;">}</span>

# Apply the DB

$ python manage.py migrate

<span style="font-family: 宋体;">如果</span><span lang="en-US"> app </span><span style="font-family: 宋体;">里面的</span><span lang="en-US"> model </span><span style="font-family: 宋体;">有变动</span><span lang="en-US">: </span><span style="font-family: 宋体;">需要</span> <span style="font-family: 宋体;">先执行</span><span lang="en-US"> makemigrations</span>

<!-- OutlineGroupNode is not supported -->

# Enable admin

# 重新定义 admin 对象的样式

 create a model admin object, then pass it as the second argument to <span style="font-family: Fira Mono; font-size: 13pt; color: #0c4b33; background-color: white; font-weight: bold;">admin.site.register()</span> – any time you need to change the admin options for an object.

![](/img/onenote-568d41e43c1c50.41249397.png)

