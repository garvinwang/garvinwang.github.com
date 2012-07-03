---
layout: post
category : tech
title: 个人免费站点建设方案
---

**[GitHub](http://www.github.com)**是基于git技术的文档管理站点，非常的实用，并且可以基于其服务免费建立个人的站点，详细介绍请参考文档 **[GotGitHub](http://www.worldhello.net/gotgithub/)**

Jekyll使用的是**[liquid模版语法](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers)**

**[Markdown使用简单的语法](http://wowubuntu.com/markdown/)**，让作者更多的关注内容，而不是展现形式

在jekyll 中有很多命令是可以快速使用的 新建一个文章 rake post title=”Hello Laird!”

这个时候就可以去_post 下编辑日期+你的title名字的文章 ##本地还有rake命令支持

rake page				# Create a new page.

rake post				# Begin a new post in ./_posts

rake preview			# Launch preview environment

rake theme:install		# Install theme

rake theme:package		# Package theme

rake theme:switch		# Switch between Jekyll-bootstrap themes.

代码高亮：

   \{\% highlight sh \%\}


   \{\% endhighlight \%\}

去掉斜杠就行了

