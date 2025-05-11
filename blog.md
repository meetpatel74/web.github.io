---
layout: default
title: Blog
---

# Blog Posts

## Latest Articles

{% for post in site.posts %}

<article class="blog-post">
    <h2><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h2>
    <div class="post-meta">
        <span class="date">{{ post.date | date: "%B %d, %Y" }}</span>
        {% if post.categories %}
        <span class="categories">
            Categories: {{ post.categories | join: ", " }}
        </span>
        {% endif %}
    </div>
    <div class="post-excerpt">
        {{ post.excerpt }}
    </div>
    <a href="{{ post.url | relative_url }}" class="read-more">Read More</a>
</article>
{% endfor %}

## Categories

- Web Development
- Programming
- Technology
- Career
- Tutorials
