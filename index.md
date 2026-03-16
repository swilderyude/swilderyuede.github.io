---
layout: default
title: Swilderyu 的个人博客
---

<div class="jumbotron">
  <h1 class="display-4">欢迎来到 Swilderyu 的个人博客</h1>
  <p class="lead">记录计算机研究生的学习、科研与项目实践</p>
  <hr class="my-4">
  <p>这里分享关于人工智能、算法设计、系统开发等领域的技术笔记、科研思考和项目经验，希望能与大家共同学习进步。</p>
  <a class="btn btn-primary btn-lg" href="/categories/research/" role="button">查看科研内容</a>
  <div class="poem">独有南山桂花发，飞来飞去袭人裾</div>
</div>

<h2>最近文章</h2>
<div class="posts-list">
  {% for post in site.posts limit:5 %}
  <article class="mb-4">
    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
    <div class="meta">
      {{ post.date | date: '%Y年%m月%d日' }} | 
      {% if post.categories and post.categories.size > 0 %}
        {% assign cat = post.categories | first %}
        <a href="/categories/{{ cat }}/">{{ cat }}</a>
      {% else %}
        未分类
      {% endif %}
    </div>
    <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
  </article>
  {% endfor %}
</div>