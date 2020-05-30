---
title: Hexo的安装使用及Github部署
date: 2019-11-17 17:17:45
tags: Hexo
categories: Hexo
index_img: /img/hexo.jpeg
---

<font color="#DC143C ">  **本文用来不定时更新** </font>

<!--more-->

# 文档加载图片

## markdown语法加载
1. 找到hexo下的 _config.yml 文件，本机的存储位置
```
 D:\00 DATA\08 HEXO blog\blog\ _config.yml
```
2. 找到 post_asset_folder 属性，将其改为 true
```
 post_asset_folder: true 
```
3. 使用指令  
```
 hexo n "博客文章的名字"
```
   新建一个博客，在路径
```
 \source\_posts 
```
下生成两个文件，分别为.md文件和其同名文件夹，将需要放在文章中的图片拷贝在同名文件夹中

4. 在.md文件中使用以下代码添加图片
```markdown
![图片描述](图片名称) 
```
上述的图片名称 可以直接写出图片的名称及类型，在文章中就可以正常显示。

## 官方加载
markdown语法加载图像的方式，在博客首页无法正常显示。所以这里给出另一种加载图像的方式，来解决上述问题。
[官网文档](https://hexo.io/zh-cn/docs/asset-folders)给出的标签插件方法加载图片，仍按照上述1~3步骤来配置，第4部在编写.md文件时，插入图像语法修改为：

```
{% asset_img 图像名.图像类型 图像名称 %}
```
上述的加载方式在博客首页和文章内部都可以正常显示。

# 修改博客背景

修改文件 post.styl,存储位置

> D:\00 DATA\08 HEXO blog\blog\themes\next\source\css\_common\components\post\post.styl