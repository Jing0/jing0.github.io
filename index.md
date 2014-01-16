---
layout: page
title: Say Hello to My New Blog!
tagline: --read & think
---
{% include JB/setup %}

Welcome to Jing0's blog!

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string}}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
{{ post.content | strip_html | truncate:100}}
<a href="{{ post.url }}">Read more</a>
{% endfor %}
</ul>

![image](http://jing0-github-io.qiniudn.com/QR.png)

