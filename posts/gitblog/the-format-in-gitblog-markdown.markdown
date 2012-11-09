---
tags: GitBlog
category: WEB开发
status: published
visibility: self
title: GitBlog markdown格式说明
---

本文对 GitBlog 中采用 markdown 的格式予以说明，以便更好的使用 GitBlog 来管理您的文章。

## 结构组成

GitBlog 中使用的 markdown 文件由两部分组成，包括Meta信息头和文章内容。其中Meta信息头对当前文档进行必要的描述，以便GitBlog能够知道如何处理您的
文章。文章内容与平常的 markdown 文件格式无异，您可以自由编写。

### Meta 信息头

Meta信息头出现在每个markdown文件的开头，由两行`---`分隔。

* title 		指定文章标题，此项必填
* category 		文章所属分类，默认不指定分类
* status 		指定文章发布状态，可选 published, stacked 默认stacked 表示不发布
* tags 			指定文章的标签，可有可无，多个标签用‘,’隔开
* visibility 	指定文章的可见性，可选 self, all 默认all。表示所有人可见

### 文章内容

该部分内容按照markdown语法格式编写即可，值得注意的是标题应从二级标题开始，不要在该部分使用一级标题。
