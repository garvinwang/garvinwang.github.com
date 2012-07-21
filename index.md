---
layout: page
title: 首页
tagline: 
---

<div class="row">
	<div class="span2">
		<img src="/images/cream_happy_ice.png"/>
	</div>
	<div class="span10">
		<h3>欢迎</h3> 
		<span>来到我的个人主页，我将在这里分享关于技术学习知识，关于团队管理的思考，关于生活体验的点滴...</span>
		<p> </p>
		<blockquote>
			<small>人生到处知何似，</small><small>恰似飞鸿踏雪泥，</small><small>泥上偶然留指爪，</small><small>鸿飞哪复计西东？ </small>
		</blockquote>
	</div>

</div>

<div class="row">
    <div class="span8">
	<div class="alert alert-error">
	<h4>最新文章</h4>
	</div>

	<ul class="posts">
	  {% for post in site.posts %}
	   <li><h3><small> {{ post.date  | date: "%Y-%m-%d "}}：</small><a href="{{ post.url }}">{{ post.title }}</a></h3></li>
	 {% endfor %}
	</ul>

    </div>
    <div class="span4">
	<div class="alert alert-sucess">
	    <h4>优秀博客</h4>
	</div>
	<ul>
	    <li><a href="http://chxt6896.github.com/" rel="nofollow">浩宇啸天 MISS 武昌鱼</a></li>
	    <li><a href="http://coolshell.cn/" rel="nofollow">CoolShell</a></li>
	    <li><a href="http://mindhacks.cn/" rel="nofollow">刘未鹏|MIND HACKS</a></li>
	    <li><a href="http://www.ruanyifeng.com/blog/" rel="nofollow">阮一峰的网络日志</a></li>
	    <li><a href="http://www.mifengtd.cn/" rel="nofollow">褪墨</a></li>
	</ul>

	<div class="alert alert-sucess">
	    <h4>联系我</h4>
	</div>
	<div>
	    <h4>Email: wanghai1024.com<small>[at]</small>gmail.com</h4>
	</div>
    </div>
</div>
