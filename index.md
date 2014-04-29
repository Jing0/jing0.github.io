---
layout: page
title: Welcome to Jing0's blog!
description: This is Jing0's blog.I share coding,reading,music and some thoughts about life here.
keywords: iOS,Mac,iPhone,Apple,Code,Program,Eliza,C,Go,Github,Vim,Music,Reading,Jackie Kuo,音乐，编程，读书，阅读
tagline: --read & think
---
{% include JB/setup %}
    
## Posts List

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

## Projects

* [Web Terminal](http://web-terminal.qiniudn.com/)-- a Terminal Simulator based on web page
* [Happy New Year](http://happy-new-year-from-jackie.u.qiniudn.com/)-- a web page to celebrate new year's coming
* [Web Bookmarks](http://mybookmarks.u.qiniudn.com/)-- just a web page for myself

## Contact Me

* [Email](mailto:j.kuo2012@gmail.com)
* [Github](https://github.com/jing0)
* [Twitter](https://twitter.com/jok3rME)

![image](http://jing0-github-io.qiniudn.com/QR.png)

<script src="https://gist.github.com/Jing0/11403855.js"></script>