---
layout: page
title: Welcome to Jing0's blog!
tagline: --read & think
---
{% include JB/setup %}

####Blog
** Recent Posts **

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string}}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
{{ post.content | strip_html | truncate:100}}
<a href="{{ post.url }}">Read more</a>
{% endfor %}
</ul>
####Project
* [Web Terminal](http://web-terminal.qiniudn.com/)-- a Terminal Simulator based on web page
* [Happy New Year](http://happy-new-year-from-jackie.u.qiniudn.com/)-- a web page to celebrate new year's coming
* [Web Bookmarks](http://mybookmarks.u.qiniudn.com/)-- just a web page for myself

####To-do
* ~~Top Secret~~

####Contact
* [Email](mailto:j.kuo2012@gmail.com)
* [Github](http://jing0.github.com)
* [Facebook](https://www.facebook.com/jackie.kuo.18)
* [Twitter](https://twitter.com/jok3rME)



![image](http://jing0-github-io.qiniudn.com/QR.png)

