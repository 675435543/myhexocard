---
title: 如何解决IDEA启动过慢的问题
date: 2019-05-05 20:33:15
categories: 软件相关
tags: [IntelliJ-IDEA,安装部署]
---

# 找到配置文件
idea的bin目录下有个.vmoptions后缀结尾的文件，请打开。
32位的对应idea.exe.vmoptions，64位的对应idea64.exe.vmoptions

# 我的配置
-server
-Xms2g
-Xmx2g
-XX:ReservedCodeCacheSize=240m
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=50
-ea
-Dsun.io.useCanonCaches=false
-Djava.net.preferIPv4Stack=true
-Djdk.http.auth.tunneling.disabledSchemes=""
-XX:+HeapDumpOnOutOfMemoryError
-XX:-OmitStackTraceInFastThrow
-javaagent:D:\idea2018\ideaIU-2018.3.win\bin\JetbrainsIdesCrack-3.4-release-enc.jar

# 程序使用内存设置
-Xms用来设置程序初始化时内存栈的大小，增加这个值会使程序的启动性能会得到提高
-Xmx用来设置程序能够使用的最大内存，这个值不要设置超过机器的内存，笔者认为，在大多数情况下,把Xmx值设置在2g和3g之间是最佳的。这里统一设置成2g
