---
layout: post
title: spark重启后metastore的问题
date: 2020-04-30
comments: true
---


spark任务重启后，可能遇到上个任务metastore没有删除的问题，需要在运行目录下删除这个文件或者文件夹