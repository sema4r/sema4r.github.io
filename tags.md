---
layout: default
title: Tags
permalink: /tags/
---

<h1>Tags</h1>

{% assign all_tags = site.tags | sort %}

{% for tag in all_tags %}
  <h2 id="{{ tag[0] | slugify }}">{{ tag[0] }}</h2>
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
