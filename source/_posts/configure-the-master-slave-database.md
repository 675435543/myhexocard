---
title: mysql5.7配置主从数据库
date: 2019-11-15 16:32:40
categories: 软件相关
tags: [Mysql,安装部署]
---

# 配置前需要阅读的文档
请先阅读[《windows环境同时安装mysql5.7和mysql8.0详细教程》](https://javahikers.github.io/2019/06/22/installs-both-mysql5.7-and-mysql8.0/),后面将按照上述教程安装5.7版本的mysql。

# 准备安装文件和配置文件
准备好两份解压之后的文件 mysql-5.7.26-winx64，一个当主库，一个当从库
准备好两份配置文件my.ini，主库一份，从库一份
主库的配置，点击[下载主库配置文件](/download/master/my.ini)

    [client]
    # 设置mysql客户端连接服务端时默认使用的端口
    port=3306
    default-character-set=utf8mb4
    [mysqld]
    #设置3306端口
    port=3306
    # 设置mysql的安装目录
    basedir =E:/software_javahiker/mysql/mysql-5.7.26-winx64
    # 设置mysql数据库的数据的存放目录
    datadir =E:/software_javahiker/mysql/mysql-5.7.26-winx64/data
    tmpdir =E:/software_javahiker/mysql/mysql-5.7.26-winx64/data
    socket=E:/software_javahiker/mysql/mysql-5.7.26-winx64/data/mysql.sock
    log-error=E:/software_javahiker/mysql/mysql-5.7.26-winx64/data/mysql_error.log
    # 服务端使用的字符集默认为utf8mb4
    character-set-server=utf8mb4
    # 创建新表时将使用的默认存储引擎
    default-storage-engine=INNODB
    # 允许最大连接数
    max_connections=200
    # 允许连接失败的次数。
    max_connect_errors=10
    # 默认使用“mysql_native_password”插件认证
    #mysql_native_password
    default_authentication_plugin=mysql_native_password
    # 主库配置
    server-id=1
    log-bin=master-bin
    log-bin-index=master-bin.index
    [mysql]
    # 设置mysql客户端默认字符集
    default-character-set=utf8mb4

从库的配置，点击[下载从库配置文件](/download/slave/my.ini)

    [client]
    # 设置mysql客户端连接服务端时默认使用的端口
    port=3307
    default-character-set=utf8mb4
    [mysqld]
    #设置3306端口
    port=3307
    # 设置mysql的安装目录
    basedir =E:/software_javahiker/mysql/mysql-5.7.26-winx64-slave
    # 设置mysql数据库的数据的存放目录
    datadir =E:/software_javahiker/mysql/mysql-5.7.26-winx64-slave/data
    tmpdir =E:/software_javahiker/mysql/mysql-5.7.26-winx64-slave/data
    socket=E:/software_javahiker/mysql/mysql-5.7.26-winx64-slave/data/mysql.sock
    log-error=E:/software_javahiker/mysql/mysql-5.7.26-winx64-slave/data/mysql_error.log
    # 服务端使用的字符集默认为utf8mb4
    character-set-server=utf8mb4
    # 创建新表时将使用的默认存储引擎
    default-storage-engine=INNODB
    # 允许最大连接数
    max_connections=200
    # 允许连接失败的次数。
    max_connect_errors=10
    # 默认使用“mysql_native_password”插件认证
    #mysql_native_password
    default_authentication_plugin=mysql_native_password
    # 从库配置
    server-id=2
    relay-log-index=slave-relay-bin.index
    relay-log=slave-relay-bin
    [mysql]
    # 设置mysql客户端默认字符集
    default-character-set=utf8mb4

# 安装    
阅读 [教程](https://javahikers.github.io/2019/06/22/installs-both-mysql5.7-and-mysql8.0/) 进行安装，参照5.7版本进行安装。

# 配置主库和从库
1. 打开主库，查看主库信息


    show master status
    
    File    Position    Binlog_Do_DB    Binlog_Ignore_DB    Executed_Gtid_Set
    master-bin.000003   154 


2. 打开从库, 根据主库信息配置从库信息后，重启服务


    CHANGE MASTER TO
    MASTER_HOST = 'localhost',
    MASTER_USER = 'root',
    MASTER_PASSWORD = '123456',
    MASTER_LOG_FILE = 'master-bin.000003',
    MASTER_LOG_POS = 154;


3. 查看从库信息，保证slave_sql_running和Slave_IO_Running都是yes


    show slave status


有疑问请移步至[MySQL数据同步，出现Slave_SQL_Running：no和slave_io_running：no问题的解决方法](https://www.cnblogs.com/l-hh/p/9922548.html)
