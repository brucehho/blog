---
layout: page
title: 标签
permalink: /tags/
---

{% assign zh_posts = site.posts | where: "lang", "zh" %}
{% assign all_tags = "" | split: "" %}
{% for post in zh_posts %}
  {% unless post.homepage == false %}
    {% for t in post.tags %}
      {% assign all_tags = all_tags | push: t %}
    {% endfor %}
  {% endunless %}
{% endfor %}
{% assign all_tags = all_tags | uniq %}

{% for t in all_tags %}
  {% assign t_url = t | uri_escape %}
  - [{{ t }}]({{ '/tags/' | append: t_url | append: '/' | relative_url }})
{% endfor %}
