---
layout: default
title: Tags
permalink: /tags/
---

<h2>Tags</h2>
<br>
{% assign all_tags = site.tags | sort %}

{% for tag in all_tags %}
  <h3 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h3>
  <ul>
    {% assign tagged_posts = tag[1] | sort: "date" | reverse %}
    {% for post in tagged_posts %}
      <li>
        <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        <span class="post-date"> — {{ post.date | date: "%d %B %Y" }}</span>
      </li>
    {% endfor %}
  </ul>
{% endfor %}
