---
layout: page
title: 王海的个人网站首页
tagline: 有中文了
---

<div class="row">
<div class="alert alert-info">
<h4>欢迎</h4> 来到我的个人主页，我将在这里分享关于技术学习知识，关于团队管理的思考，关于生活体验的点滴...
</div>
</div>

<div class="row">
    
	<div class="alert alert-error">
	<h4>最新文章</h4>
	</div>
	<ul class="posts">
	  {% for post in site.posts %}
	   <li><strong><a href="{{ post.url }}">{{ post.title }}</a></strong>...{{ post.date  | date: "%Y-%m-%d "}}</li>
	 {% endfor %}
	</ul>
</div>
<!--
<div class="span8">
	<h3>文章列表</h3>
>奇怪了
</div>

<div class="span4">

</div>

-->