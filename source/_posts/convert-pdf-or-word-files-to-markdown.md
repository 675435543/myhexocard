---
title: PDF或是word文件如何转成markdown格式
date: 2019-09-18 23:05:49
categories: 其他
tags: [总结,使用教程]
---

# 安装包

链接：https://pan.baidu.com/s/1GqiUOvN2ideaAGZUpn8OxA 
提取码：tmkk 
pdfedplu.rar 将pdf转word的，typora0.9_zh.rar 将word转markdown，另外一个是依赖的安装包

# PDF导出成word
利用  PDFXEditPortable.exe 将PDF 导出成 word 格式，文件名为 xx.docx

# word导出成 markdown 源代码
使用 typora 获得该 word 文档的 markdown 源代码

文件->导入 ，找到word文档，点打开即可获得 markdown 源代码

如果原始的 word 文档里包含图片，这些图片以本地图片的形式存在于 markdown 里。

格式是这样的：

`![](media/image1.png){width="5.768055555555556in" height="2.057638888888889in"}`

此时，如果直接将包含了这些本地图片的标签的 markdown 发布到简书或是CSDN。这些本地图片将无法显示。

# 替换本地图片链接
## 手工替换
将图片上传到网络，如新浪图床。这里推荐大家在google浏览器里面安装新浪图床插件，然后将图片上传到新浪图床。至于怎么安装请自行百度。打开新浪图床是如下页面。

![image01.png](https://ww1.sinaimg.cn/large/80673b2agy1g743m5lef8j20wo0mddgv.jpg)

将图片拖拽上去之后会生成一个链接，如下，复制markdown下的链接将本地图片格式替换即可

![image02.png](https://ww1.sinaimg.cn/large/80673b2agy1g74f6y5ofyj20wm0mr40t.jpg)

## 脚本替换
如果觉得手动替换链接麻烦，这里推荐一种自动替换链接的方式。熟练操作之后也很方便。

将上面生成的markdown链接复制好。 如果有多个图片，按照图片出现的顺序，将链接依次排好

![image1.png]...

![image2.png]...

![image3.png]...

放到步骤3生成的markdown源码的顶部，然后用脚本自动替换。脚本我已经给出来了。点击[下载脚本](/download/markdown_tool.rar)
1会替换第1张本地图片，2会替换第2张本地图片，3会替换第3张本地图片，依次类推。

按照如下步骤，右边是替换之后的markdown源码。

![image03.png](https://ww1.sinaimg.cn/large/80673b2agy1g74gg9wjdrj214w0m2adc.jpg)


