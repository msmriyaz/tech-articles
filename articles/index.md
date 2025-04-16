---
layout: default
title: All Articles
excerpt: Browse our complete collection of technical articles
---

<article>
  <h1>All Technical Articles</h1>
  
  <p>This page provides an overview of all the technical articles in our collection. Browse the list to find topics that interest you or use the search function to find specific information.</p>

  <h2>Article Categories</h2>

  <p>Our articles are organized into the following categories:</p>

  <ul>
    <li><strong>Getting Started</strong> - Introductory articles for beginners</li>
    <li><strong>Tutorials</strong> - Step-by-step guides for specific tasks</li>
    <li><strong>Best Practices</strong> - Recommendations for efficient and effective development</li>
    <li><strong>Advanced Topics</strong> - In-depth articles for experienced readers</li>
  </ul>

  <h2>Complete Article List</h2>

  <div class="article-list">
    {% assign sorted_posts = site.posts | sort: 'date' | reverse %}
    {% for post in sorted_posts %}
    <div class="article-item">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p class="date"><strong>Posted on:</strong> {{ post.date | date: "%B %-d, %Y" }}</p>
      {% if post.excerpt %}<p>{{ post.excerpt }}</p>{% endif %}
      <p><a href="{{ post.url | relative_url }}">Read more →</a></p>
      <hr>
    </div>
    {% endfor %}
  </div>

  <h2>Interested in Contributing?</h2>

  <p>If you'd like to contribute your own technical article to our collection, please check our <a href="/contributing">contribution guidelines</a> for details on our submission process and formatting requirements.</p>
</article>

<style>
  .article-list {
    margin: 2rem 0;
  }
  .article-item {
    margin-bottom: 2rem;
  }
  .date {
    color: #666;
    font-size: 0.9rem;
    margin-bottom: 0.5rem;
  }
  hr {
    border: 0;
    height: 1px;
    background-color: #e0e0e0;
    margin: 1.5rem 0;
  }
</style> 