---
layout: default
title: "Archive"
permalink: /archive/
---

<section class="archive-container">
  <h2>Archive</h2>
  <p class="archive-intro">All past daily briefings, ordered chronologically.</p>

  <ul class="archive-list">
    {% for post in site.posts %}
      <li>
        <a href="{{ post.url | relative_url }}" class="archive-link">
            <time class="archive-date" datetime="{{ post.date | date_to_xmlschema }}">
                {{ post.date | date: "%B %d, %Y" }}
            </time>
        </a>
      </li>
    {% endfor %}
  </ul>
</section>
