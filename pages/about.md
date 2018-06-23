---
layout: page
title: About
description: 分享生活趣事，记录笔记心得。
keywords: Jinbo, 随心
comments: true
menu: 关于
permalink: /about/
---
## 很多有意义的事：想做，但是未做

##### 坚持晚上跑步

##### 坚持看杂书

##### 坚持写文字

## 联系

{% for website in site.data.social %}
* {{ website.sitename }}：[@{{ website.name }}]({{ website.url }})
{% endfor %}

## Skill Keywords

{% for category in site.data.skills %}
### {{ category.name }}
<div class="btn-inline">
{% for keyword in category.keywords %}
<button class="btn btn-outline" type="button">{{ keyword }}</button>
{% endfor %}
</div>
{% endfor %}
