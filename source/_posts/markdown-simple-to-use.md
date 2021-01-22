---
title: markdown简明使用方法
date: 2019-05-04 21:34:16
categories: 其他
tags: [使用教程,总结]
---
一行语法对应一行示例,学会之后即可轻松写出高大上的文档。本人使用sublime编写，只为简洁。
***
# 强调
## 斜体，单星号或单下划线，可跨行
\*作者最新文章\*
*作者最新文章*
\_机器监测员工绩效、发出解雇指令\_
_机器监测员工绩效、发出解雇指令_
\_机器监测员工绩
效、发出解雇指令\_
_机器监测员工绩
效、发出解雇指令_
## 粗体，双星号或双下划线，可跨行
\*\*北京延庆街头世园会气氛渐浓\*\*
**北京延庆街头世园会气氛渐浓**
\_\_亚马逊会员为什么会如此成功？\_\_
__亚马逊会员为什么会如此成功？__
\_\_亚马逊会员为
什么会如此成功？*__*
__亚马逊会员为
什么会如此成功？__

***
# 分割线
## 三个或更多*_-，必须单独一行
\*\*\* 3个*
\_\_\_ 3个_
\-\-\- 3个-


***
# 引用
## 引用翻译成html就是<blockquote\></blockquote\>
\>我是引用
>我是引用

\>我是引用
 \>\>我是引用中的引用
>我是引用
 >>我是引用中的引用

***
# 标题：Setext方式
大标题
*===*
大标题
===
小标题
\-\-\-
小标题
---

***
# 标题：Atx方式
*#* 一级标题
*##* 二级标题
*###* 三级标题
*####* 四级标题
*#####* 五级标题
*######* 六级标题
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

***
# 无序列表
## -+*，后面有空格
\- 无序列表
\- 无序列表
\- 无序列表
- 无序列表
- 无序列表
- 无序列表

\+ 无序列表
\+ 无序列表
\+ 无序列表
+ 无序列表
+ 无序列表
+ 无序列表

\* 无序列表
\* 无序列表
\* 无序列表
* 无序列表
* 无序列表
* 无序列表

***
# 有序列表
## 数字（可无序），点， 空格
1\. 有序列表
2\. 有序列表
3\. 有序列表
8\. 有序列表

1. 有序列表
2. 有序列表
3. 有序列表
8. 有序列表

***
# 嵌套列表
## -+*可交叉使用，符号前后带空格
\-&nbsp;嵌套列表
&nbsp;\+&nbsp;嵌套列表
&nbsp;\+&nbsp;嵌套列表
&nbsp;&nbsp;\-&nbsp;嵌套列表
&nbsp;&nbsp;&nbsp;\*&nbsp;嵌套列表
-&nbsp;嵌套列表

- 嵌套列表
 + 嵌套列表
 + 嵌套列表
  - 嵌套列表
   * 嵌套列表
- 嵌套列表

***
# 文字超链：Inline方式
`[javahiker](https://javahikers.gitee.io "javahiker的博客")`
[javahiker](https://javahikers.gitee.io "javahiker的博客")

***
# 图片超链
`![Github Javahiker](https://javahikers.gitee.io/2019/05/04/markdown-simple-to-use/javahiker.jpg "Javahiker")`
![Github Javahiker](https://javahikers.gitee.io/2019/05/04/markdown-simple-to-use/javahiker.jpg "Javahiker")
在hexo中引入图片的其他方法，请进入我的博文=> [hexo博客引入图片](https://javahikers.gitee.io/2019/06/12/hexo-blog-introduces-images/ "javahiker和你一起进步")

***
# 索引超链接 Reference方式
## 1，2可以是任意字符
`[javahiker][1]`
`![Github Javahiker][2]`

`[1]:https://javahikers.gitee.io`
`[2]:https://javahikers.gitee.io/2019/05/04/markdown-simple-to-use/javahiker.jpg`
***
[javahiker][1]
![Github Javahiker][2]

[1]:https://javahikers.gitee.io
[2]:https://javahikers.gitee.io/2019/05/04/markdown-simple-to-use/javahiker.jpg

***
# 自动链接
## 尖括号
`<https://javahikers.gitee.io>`
`<675435543@qq.com>`
***
<https://javahikers.gitee.io>
<675435543@qq.com>

***
# 代码：行内代码
## 使用左上角数字1左边的键盘
\`val s = "hello Markdown"\`
\`println( s )\`
`val s = "hello Markdown"`
`println( s )`

***
# 代码：段落代码
## 每行文字前加4个空格或者1个Tab
&nbsp;&nbsp;&nbsp;&nbsp;val s = "hello Markdown"
&nbsp;&nbsp;&nbsp;&nbsp;println( s )

    val s = "hello Markdown"
    println( s )

***
# 注释
<\!-- 注释 -->

***
# 转义字符
Markdown中的转义字符为\，转义的有：
\\\ 反斜杠
\\` 反引号
\\* 星号
\\_ 下划线
\\{\\} 大括号
\\[\\] 中括号
\\(\\) 小括号
\\# 井号
\\+ 加号
\\- 减号
\\. 英文句号
\\! 感叹号

***
# 其它
## 文本中可直接用html标签