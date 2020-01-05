---
title: hexo博客引入图片
date: 2019-06-12 21:01:23
categories: 其他
tags: [Hexo,安装部署]
---
# 前言
很多时候图片比文字更有说服力，但是如何引入呢？图片放什么地方呢？其实不用借助七牛。

***
# 步骤
1. 将_config.yml里的post_asset_folder设置为true
`post_asset_folder: true`
2. 在hexo目录下执行:
`npm install hexo-asset-image --save`
3. 在hexo目录下执行:
`hexo n "博客名"`
_post目录下会生成一个名称为"博客名.md"的博客，同时也会生成一个与博客同名的文件夹"博客名"
4. 将要上传的图片放到博客对应的文件夹下，然后在博客中使用markdown的格式引入图片
`![提示信息](博客名/图片名.jpg)`
提醒：这种方法只是单纯把图片显示出来，如果图片很大的话就会铺满屏幕或者超高，排版上不好看
+ 通过img标签控制宽高
`<img src="hexo-blog-introduces-images/Daniel.jpg" width="460px" height="690px" />`
+ 通过 div 标签和 align 属性控制对齐方式
`<div align="center">`
`<img src="hexo-blog-introduces-images/Daniel.jpg" width="460px" height="690px" />`
`</div>`

5. hexo g部署之后，进入public\2019\06\12\博客名\index.html文件中查看
html标签内的语句是`<img src="2019/06/12/博客名/图片名.jpg">`
而不是`<img src="博客名/图片名.jpg>`
6. 这里碰到一个问题，无论本地还是线上，生成的index.html生成的img标签是`<img src="/.io//图片名.jpg">`，怀疑是hexo-asset-image版本的问题。查看我的hexo-asset-image版本是1.0.0，选择降低版本后问题解决
`npm install hexo-asset-image@0.0.3 --save`
***
来张Daniel的帅照~~~
<div align="center">
<img src="hexo-blog-introduces-images/Daniel.jpg" width="460px" height="690px" alt="不好啦，图片不见啦~~" title="你是我的粉丝吗"/>
</div>
