---
title: IDEA搭建maven多模块module项目
date: 2019-06-14 06:20:23
categories: 其他
tags: [IntelliJ-IDEA,Maven,使用教程]
---

通过IDEA创建多模块项目，有时候需要树形结构，有的需要平行结构，下面将手把手教你如何创建多模块项目。
### 新建项目
#### 打开IDEA新建项目
<div align="center">
<img src="IDEA搭建maven多模块module项目/01.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 用maven创建项目，点击next 进入下一步
<div align="center">
<img src="IDEA搭建maven多模块module项目/02.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 建立groupId,artifactId,version信息
<div align="center">
<img src="IDEA搭建maven多模块module项目/03.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 建项目名与项目位置
<div align="center">
<img src="IDEA搭建maven多模块module项目/04.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 建好的项目目录如下，红框内的文件可以删除或是保留
<div align="center">
<img src="IDEA搭建maven多模块module项目/05.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 删除多余的文件
<div align="center">
<img src="IDEA搭建maven多模块module项目/06.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
### 创建子模块，父子模块之间是树形结构
#### 新建模块
<div align="center">
<img src="IDEA搭建maven多模块module项目/07.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 选择Maven,点Next
<div align="center">
<img src="IDEA搭建maven多模块module项目/08.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 选择父模块
<div align="center">
<img src="IDEA搭建maven多模块module项目/09.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### ArtifactId对应模块名称
<div align="center">
<img src="IDEA搭建maven多模块module项目/10.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 填写子模块名称
<div align="center">
<img src="IDEA搭建maven多模块module项目/11.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 生成树形结构的父子模块

<div align="center">
<img src="IDEA搭建maven多模块module项目/12.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
### 创建子模块，父子模块之间是平行结构
#### 重复之前创建子模块的步骤，直到填写子模块名称 这一步，让子模块跟跟父模块处于平行的目录

<div align="center">
<img src="IDEA搭建maven多模块module项目/13.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

---
#### 生成平行结构的父子模块
<div align="center">
<img src="IDEA搭建maven多模块module项目/14.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

***
### IDEA删除模块，然后再创建时出现异常
删除模块，然后再创建相同名称的模块时，往往会提示：

        Maven:Failed to create a Maven project ‘…pom.xml’ already exists in VFS

* 模块都已经删除了，怎么还提示我有相同的工程呢？

* 原因，原先的那个Project其实还是在我们的电脑上，即VFS虚拟档案系统。

* 解决办法

<div align="center">
<img src="IDEA搭建maven多模块module项目/15.png" alt="不好啦，图片不见啦~~" title="谢谢阅读"/>
</div>

***