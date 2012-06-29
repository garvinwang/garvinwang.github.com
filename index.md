---
layout: page
title: Hello World!
tagline: Supporting tagline
---
<div class="span4">
<div id="home">
  <h1>Blog Posts</h1>
    <ul class="posts">
      {% for post in site.posts %}
       <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
     {% endfor %}
   </ul>
</div>
</div>

<div class="span8">
content
</div>
