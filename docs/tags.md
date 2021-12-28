---
layout: page
permalink: /tags/
title: tags
---

## list of tags
{% for tag in site.tags %}
{% capture tag_name %}{{ tag | first }}{% endcapture %}
* [{{ tag_name }}](#{{ tag_name }})
{% endfor %}

## posts organized by tag
{% for tag in site.tags %}
{% capture tag_name %}{{ tag | first }}{% endcapture %}
* **{{ tag_name }}** ([feed](../feed/by_tag/{{ tag_name }}.xml))
{% for post in site.tags[tag_name] %}
  * [{{ post.title }}]({{ post.url }})
{% endfor %}
{% endfor %}
