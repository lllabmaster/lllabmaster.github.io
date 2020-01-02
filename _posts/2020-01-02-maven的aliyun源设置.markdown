---
layout: post
title: maven的aliyun源设置
date: 2020-01-02
comments: true
---



```xml
<?xml version="1.0" encoding="UTF-8"?>
<settings xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 http://maven.apache.org/xsd/settings-1.0.0.xsd" xmlns="http://maven.apache.org/SETTINGS/1.0.0"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <mirrors>
    <mirror>
      <id>UK</id>
      <name>UK Central</name>
      <url>http://uk.maven.org/maven2</url>
      <mirrorOf>central</mirrorOf>
    </mirror>
    <mirror>
        <id>aliyunmaven</id>
        <mirrorOf>*</mirrorOf>
        <name>阿里云公共仓库</name>
        <url>https://maven.aliyun.com/repository/public</url>
    </mirror>
     <mirror>
        <id>aliyunmaven</id>
        <mirrorOf>*</mirrorOf>
        <name>阿里云谷歌仓库</name>
        <url>https://maven.aliyun.com/repository/google</url>
    </mirror>
    <mirror>
        <id>aliyunmaven</id>
        <mirrorOf>*</mirrorOf>
        <name>阿里云阿帕奇仓库</name>
        <url>https://maven.aliyun.com/repository/apache-snapshots</url>
    </mirror>
    <mirror>
        <id>aliyunmaven</id>
        <mirrorOf>*</mirrorOf>
        <name>阿里云spring仓库</name>
        <url>https://maven.aliyun.com/repository/spring</url>
    </mirror>
    <mirror>
        <id>aliyunmaven</id>
        <mirrorOf>*</mirrorOf>
        <name>阿里云spring插件仓库</name>
        <url>https://maven.aliyun.com/repository/spring-plugin</url>
    </mirror>
  </mirrors> 
</settings>
```