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

<script src="https://unpkg.com/simple-jekyll-search@latest/dest/simple-jekyll-search.min.js"></script>
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: '/search.json',
    searchResultTemplate: '<li style="margin-bottom: 8px;"><span style="color: #666; font-family: monospace; margin-right: 10px;">{date}</span> &raquo; <a href="{url}" style="font-weight: bold;">{title}</a></li>',
    noResultsText: 'Nie znaleziono pasujących wpisów.',
    limit: 500,
    fuzzy: false
  })
</script>
