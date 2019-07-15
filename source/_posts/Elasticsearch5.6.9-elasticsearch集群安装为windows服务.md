---
title: Elasticsearch5.6.9-elasticsearch集群安装为windows服务
date: 2019-07-14 14:23:23
categories: 分布式
tags: [安装部署,Elasticsearch]
---

在安装elasticsearch集群之前，请先阅读这篇博文《Elasticsearch5.6.9-安装使用》的这一部分[elasticsearch分布式安装](https://javahikers.github.io/2019/07/10/Elasticsearch5.6.9-%E5%AE%89%E8%A3%85%E4%BD%BF%E7%94%A8/#elasticsearch%E5%88%86%E5%B8%83%E5%BC%8F%E5%AE%89%E8%A3%85)
本文在它的基础上进行安装，配置文件elasticsearch.yml保持一致。3个文件我已打包好，点击[下载文件](/download/elasticsearch yml文件.rar)

# 进入各自的bin目录，安装并启动服务
    D:\downloadsoftware\elasticsearch\elasticsearch-5.6.9\bin>elasticsearch-service.bat install elasticsearchMaster
    D:\downloadsoftware\elasticsearch\elasticsearch-5.6.9\bin>elasticsearch-service.bat start elasticsearchMaster
    D:\downloadsoftware\elasticsearch\elasticsearch-5.6.9_slave1\bin>elasticsearch-service.bat install elasticsearchSlave1
    D:\downloadsoftware\elasticsearch\elasticsearch-5.6.9_slave1\bin>elasticsearch-service.bat start elasticsearchSlave1
    D:\downloadsoftware\elasticsearch\elasticsearch-5.6.9_slave2\bin>elasticsearch-service.bat install elasticsearchSlave2
    D:\downloadsoftware\elasticsearch\elasticsearch-5.6.9_slave2\bin>elasticsearch-service.bat start elasticsearchSlave2

安装好之后可以在windows服务窗口查看已安装的服务
<div>
![](Elasticsearch5.6.9-elasticsearch集群安装为windows服务/001.png)
</div>

# 命令
+ elasticsearch-service.bat install: 安装服务
+ elasticsearch-service.bat remove: 删除已安装的服务（如果启动则停止服务） 
+ elasticsearch-service.bat start: 启动Elasticsearch服务（如果已安装） 
+ elasticsearch-service.bat stop: 停止服务（如果已启动） 
+ elasticsearch-service.bat manager:启动GUI来管理已安装的服务
命令后面可以跟服务名称
