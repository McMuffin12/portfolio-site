---
title: /blog
layout: page
permalink: /blog/
---

# <span class="ide-keyword">Blog</span> <span class="ide-operator">&</span> <span class="ide-class">Articles</span>

<span class="ide-comment">// Thoughts on development, technology, and best practices</span>

<span class="ide-keyword">const</span> <span class="ide-variable">blog</span> <span class="ide-operator">=</span> <span class="ide-bracket">{</span>
  <span class="ide-property">purpose</span><span class="ide-operator">:</span> <span class="ide-string">"Share knowledge and learn from the community"</span><span class="ide-operator">,</span>
  <span class="ide-property">topics</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span><span class="ide-string">"JavaScript"</span><span class="ide-operator">,</span> <span class="ide-string">"React"</span><span class="ide-operator">,</span> <span class="ide-string">"Node.js"</span><span class="ide-operator">,</span> <span class="ide-string">"Best Practices"</span><span class="ide-bracket">]</span><span class="ide-operator">,</span>
  <span class="ide-property">frequency</span><span class="ide-operator">:</span> <span class="ide-string">"Weekly"</span>
<span class="ide-bracket">}</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Recent</span> <span class="ide-class">Posts</span>

<div class="blog-posts">
  {% for post in site.posts limit:10 %}
    <article class="blog-post">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title | escape }}</a></h3>
      <p class="post-meta">
        <span class="ide-comment">// Published on</span> 
        <span class="ide-property">{{ post.date | date: "%B %d, %Y" }}</span>
        {% if post.tags.size > 0 %}
          <span class="ide-comment">// Tags:</span>
          {% for tag in post.tags %}
            <span class="ide-string">{{ tag }}</span>{% unless forloop.last %}, {% endunless %}
          {% endfor %}
        {% endif %}
      </p>
      <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <p><a href="{{ post.url | relative_url }}" class="read-more">
        <span class="ide-function">readMore</span><span class="ide-bracket">()</span>
      </a></p>
    </article>
  {% endfor %}
</div>

## <span class="ide-keyword">Categories</span>

<span class="ide-keyword">const</span> <span class="ide-variable">categories</span> <span class="ide-operator">=</span> <span class="ide-bracket">[</span>
  <span class="ide-bracket">{</span> <span class="ide-property">name</span><span class="ide-operator">:</span> <span class="ide-string">"JavaScript"</span><span class="ide-operator">,</span> <span class="ide-property">count</span><span class="ide-operator">:</span> <span class="ide-number">12</span> <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span> <span class="ide-property">name</span><span class="ide-operator">:</span> <span class="ide-string">"React"</span><span class="ide-operator">,</span> <span class="ide-property">count</span><span class="ide-operator">:</span> <span class="ide-number">8</span> <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span> <span class="ide-property">name</span><span class="ide-operator">:</span> <span class="ide-string">"Node.js"</span><span class="ide-operator">,</span> <span class="ide-property">count</span><span class="ide-operator">:</span> <span class="ide-number">6</span> <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span> <span class="ide-property">name</span><span class="ide-operator">:</span> <span class="ide-string">"Python"</span><span class="ide-operator">,</span> <span class="ide-property">count</span><span class="ide-operator">:</span> <span class="ide-number">4</span> <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span> <span class="ide-property">name</span><span class="ide-operator">:</span> <span class="ide-string">"DevOps"</span><span class="ide-operator">,</span> <span class="ide-property">count</span><span class="ide-operator">:</span> <span class="ide-number">3</span> <span class="ide-bracket">}</span>
<span class="ide-bracket">]</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Popular</span> <span class="ide-class">Posts</span>

<span class="ide-comment">// Most read articles</span>
<span class="ide-keyword">const</span> <span class="ide-variable">popularPosts</span> <span class="ide-operator">=</span> <span class="ide-bracket">[</span>
  <span class="ide-string">"Understanding React Hooks: A Complete Guide"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Building Scalable Node.js Applications"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Modern JavaScript: ES2023 Features You Should Know"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Optimizing Performance in React Applications"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Docker for JavaScript Developers"</span>
<span class="ide-bracket">]</span><span class="ide-operator">;</span>

<span class="ide-comment">// Stay tuned for more content!</span>
<span class="ide-keyword">console</span><span class="ide-operator">.</span><span class="ide-function">log</span><span class="ide-bracket">(</span><span class="ide-string">"New posts published every week 📝"</span><span class="ide-bracket">)</span><span class="ide-operator">;</span>
