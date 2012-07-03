---
layout: page
title: 王海的个人网站首页
tagline: 有中文了
---

<div class="row alert alert-info">
	<div class="span12">
		<div class="row-fluid">
			<div class="span2">
				<img src="/images/cream_happy_ice.png"/>
			</div>
			<div class="span8">
				<h3>欢迎</h3> 
				<span>来到我的个人主页，我将在这里分享关于技术学习知识，关于团队管理的思考，关于生活体验的点滴...</span>
				<p> </p>
				<blockquote>
					<small>人生到处知何似，</small><small>恰似飞鸿踏雪泥，</small><small>泥上偶然留指爪，</small><small>鸿飞哪复计西东？ </small>
				</blockquote>
			</div>
		</div>
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