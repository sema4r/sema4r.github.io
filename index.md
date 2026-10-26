---
layout: default
title: Home
---

This blog will be about topics I think about from Machine Learning, Mathematical Physics and Math
in general. Some posts will be introductory, some not.

The blog title contains the famous proposition from Wittgenstein’s Tractatus Logico-Philosophicus. 
While it has a special meaning in the context of the book, it is nonetheless a pretty good guiding 
principle when dealing with science.


## Posts

<ul class="post-list">
{% for post in site.posts %}
  <li>
    <span class="post-date">
      {{ post.date | date: "%d %B %Y" }}
    </span>
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
