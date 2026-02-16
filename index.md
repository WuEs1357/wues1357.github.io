---
layout: default
title: Strona główna # Wpis tutaj tytuł strony głównej
---

<div id="all-posts">
  <h3>Spis treści:</h3>
  <ul style="list-style: none; padding-left: 0;">
    {% for post in site.posts %}
      <li style="margin-bottom: 8px;">
        <span style="color: #666; font-family: monospace; margin-right: 10px;">{{ post.date | date: "%d-%m-%Y" }}</span>
        &raquo;
        <a href="{{ post.url | relative_url }}" style="font-weight: bold;">{{ post.title }}</a>
      </li>
    {% endfor %}
  </ul>
</div>
