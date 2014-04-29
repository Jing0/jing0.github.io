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

<script src="//code.jquery.com/jquery-1.11.0.min.js"></script>
<script src="//code.jquery.com/jquery-migrate-1.2.1.min.js"></script>
<style>
.timeline {
	position: relative;
	margin-top: 60px;
	height: 60px;
}
.line {
	height: 4px;
	background-color: #888;
	width: 100%;
	top: 50%;
	margin-top: -2px;
	position: absolute;
}
.time-item {
	position: relative;
	display: inline-block;
	zoom: 1;
	margin-right: 40px;
}
.time {
	display: block;
	background-color: #1A69EC;
	color: #fff;
	border-radius: 45px;
	width: 45px;
	height: 45px;
	line-height: 45px;
	font-size: 13px;
	text-align: center;
}
.event {
	background-color: rgba(0,0,0,.8);
	padding: 10px;
	border-radius: 4px;
	-webkit-border-radius: 4px;
	display: none;
	position: absolute;
	bottom: 40px;
	color: #fff;
}
.event:before {
	content: "";
	display: block;
	position: absolute;
	bottom: -20px;
	height: 0;
	width: 0;
	overflow: hidden;
	font-size: 0;
	line-height: 0;
	border-color: rgba(0,0,0,.8) transparent transparent transparent;
	border-style: solid dashed dashed dashed;
	border-width: 40px 0 0 0;
}
.time-item:hover .event {
	display: block;
}
</style>
<div class="timeline">
		<div class="line"></div>
		<div class="time-item">
			<span class="time">1995</span>
			<div class="event">Born</div>
		</div>
		<div class="time-item">
			<span class="time">2011</span>
			<div class="event">Learned about Java and made first Android app</div>
		</div>
		<div class="time-item">
			<span class="time">2013</span>
			<div class="event">Entered University</div>
		</div>
</div>