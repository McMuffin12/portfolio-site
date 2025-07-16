---
title: /timeline
layout: page
permalink: /timeline/
---

# <span class="ide-keyword">Timeline</span> <span class="ide-operator">&</span> <span class="ide-class">Milestones</span>

<span class="ide-comment">// A chronological journey through my career and achievements</span>

<span class="ide-keyword">const</span> <span class="ide-variable">timeline</span> <span class="ide-operator">=</span> <span class="ide-bracket">{</span>
  <span class="ide-property">purpose</span><span class="ide-operator">:</span> <span class="ide-string">"Track professional growth and key achievements"</span><span class="ide-operator">,</span>
  <span class="ide-property">categories</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span><span class="ide-string">"Career"</span><span class="ide-operator">,</span> <span class="ide-string">"Projects"</span><span class="ide-operator">,</span> <span class="ide-string">"Certifications"</span><span class="ide-operator">,</span> <span class="ide-string">"Learning"</span><span class="ide-bracket">]</span><span class="ide-operator">,</span>
  <span class="ide-property">format</span><span class="ide-operator">:</span> <span class="ide-string">"Reverse chronological order"</span>
<span class="ide-bracket">}</span><span class="ide-operator">;</span>

<div class="timeline-container">
  <div class="timeline">
    {% comment %} Combine projects and posts that have timeline.show = true {% endcomment %}
    {% assign timeline_items = '' | split: '' %}
    
    {% comment %} Add projects to timeline {% endcomment %}
    {% for project in site.projects %}
      {% if project.timeline.show %}
        {% assign timeline_items = timeline_items | push: project %}
      {% endif %}
    {% endfor %}
    
    {% comment %} Add posts to timeline {% endcomment %}
    {% for post in site.posts %}
      {% if post.timeline.show %}
        {% assign timeline_items = timeline_items | push: post %}
      {% endif %}
    {% endfor %}
    
    {% comment %} Sort by date (newest first) {% endcomment %}
    {% assign sorted_timeline = timeline_items | sort: 'date' | reverse %}
    
    {% for item in sorted_timeline %}
      <div class="timeline-item">
        <div class="timeline-date">
          <span class="ide-property">{{ item.date | date: "%B %d, %Y" }}</span>
        </div>
        <div class="timeline-content">
          <h3 class="timeline-title">
            <a href="{{ item.url }}">{{ item.title }}</a>
          </h3>
          <div class="timeline-meta">
            <span class="ide-comment">// Type:</span> 
            <span class="ide-keyword">{{ item.timeline.category | capitalize }}</span>
            <span class="ide-comment">// Milestone:</span>
            <span class="ide-string">{{ item.timeline.milestone }}</span>
            
            {% if item.timeline.category == 'project' %}
              <span class="ide-comment">// Tech:</span>
              {% for tech in item.tech limit:3 %}
                <span class="ide-variable">{{ tech }}</span>{% unless forloop.last %}, {% endunless %}
              {% endfor %}
            {% elsif item.timeline.category == 'article' %}
              <span class="ide-comment">// Tags:</span>
              {% for tag in item.tags limit:3 %}
                <span class="ide-variable">{{ tag }}</span>{% unless forloop.last %}, {% endunless %}
              {% endfor %}
            {% endif %}
          </div>
          <div class="timeline-description">
            {% if item.description %}
              {{ item.description }}
            {% elsif item.excerpt %}
              {{ item.excerpt | strip_html | truncate: 150 }}
            {% endif %}
          </div>
          {% if item.timeline.impact %}
            <div class="timeline-impact">
              <span class="ide-comment">// Impact:</span>
              <span class="ide-function">{{ item.timeline.impact }}</span>
            </div>
          {% endif %}
          <div class="timeline-action">
            <a href="{{ item.url }}" class="read-more">
              {% if item.timeline.category == 'project' %}
                <span class="ide-function">viewProject</span><span class="ide-bracket">()</span>
              {% else %}
                <span class="ide-function">readArticle</span><span class="ide-bracket">()</span>
              {% endif %}
            </a>
          </div>
        </div>
      </div>
    {% endfor %}
  </div>
</div>

## <span class="ide-keyword">Categories</span>

<span class="ide-keyword">const</span> <span class="ide-variable">categories</span> <span class="ide-operator">=</span> <span class="ide-bracket">{</span>
  <span class="ide-property">projects</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span>
    <span class="ide-string">"Major project launches and releases"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Technical achievements and milestones"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Open source contributions and tools"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Beta releases and user testing phases"</span>
  <span class="ide-bracket">]</span><span class="ide-operator">,</span>
  <span class="ide-property">articles</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span>
    <span class="ide-string">"Technical tutorials and guides"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Best practices and architecture insights"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Industry analysis and trend reviews"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Open source project documentation"</span>
  <span class="ide-bracket">]</span><span class="ide-operator">,</span>
  <span class="ide-property">impact</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span>
    <span class="ide-string">"Metrics tracked from project launches"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Reader engagement and community feedback"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Performance improvements and optimizations"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Knowledge sharing and developer education"</span>
  <span class="ide-bracket">]</span>
<span class="ide-bracket">}</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Statistics</span>

<span class="ide-comment">// Overview of timeline metrics</span>

<div class="timeline-stats">
  {% assign timeline_projects = site.projects | where: 'timeline.show', true %}
  {% assign timeline_posts = site.posts | where: 'timeline.show', true %}
  {% assign total_timeline = timeline_projects.size | plus: timeline_posts.size %}
  
  <div class="stat-item">
    <div class="stat-value">{{ total_timeline }}</div>
    <div class="stat-label">Total Milestones</div>
  </div>
  <div class="stat-item">
    <div class="stat-value">{{ timeline_projects.size }}</div>
    <div class="stat-label">Projects</div>
  </div>
  <div class="stat-item">
    <div class="stat-value">{{ timeline_posts.size }}</div>
    <div class="stat-label">Articles</div>
  </div>
  <div class="stat-item">
    <div class="stat-value">{{ site.projects | where: 'featured', true | size }}</div>
    <div class="stat-label">Featured Work</div>
  </div>
</div>

## <span class="ide-keyword">Skills</span> <span class="ide-class">Evolution</span>

<span class="ide-comment">// How my skills have developed over time</span>

<span class="ide-keyword">const</span> <span class="ide-variable">skillsEvolution</span> <span class="ide-operator">=</span> <span class="ide-bracket">[</span>
  <span class="ide-bracket">{</span>
    <span class="ide-property">period</span><span class="ide-operator">:</span> <span class="ide-string">"2019-2020"</span><span class="ide-operator">,</span>
    <span class="ide-property">focus</span><span class="ide-operator">:</span> <span class="ide-string">"Frontend Development"</span><span class="ide-operator">,</span>
    <span class="ide-property">skills</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span><span class="ide-string">"HTML"</span><span class="ide-operator">,</span> <span class="ide-string">"CSS"</span><span class="ide-operator">,</span> <span class="ide-string">"JavaScript"</span><span class="ide-operator">,</span> <span class="ide-string">"React"</span><span class="ide-bracket">]</span>
  <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span>
    <span class="ide-property">period</span><span class="ide-operator">:</span> <span class="ide-string">"2020-2022"</span><span class="ide-operator">,</span>
    <span class="ide-property">focus</span><span class="ide-operator">:</span> <span class="ide-string">"Full-Stack Development"</span><span class="ide-operator">,</span>
    <span class="ide-property">skills</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span><span class="ide-string">"Node.js"</span><span class="ide-operator">,</span> <span class="ide-string">"Python"</span><span class="ide-operator">,</span> <span class="ide-string">"PostgreSQL"</span><span class="ide-operator">,</span> <span class="ide-string">"API Design"</span><span class="ide-bracket">]</span>
  <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span>
    <span class="ide-property">period</span><span class="ide-operator">:</span> <span class="ide-string">"2022-2024"</span><span class="ide-operator">,</span>
    <span class="ide-property">focus</span><span class="ide-operator">:</span> <span class="ide-string">"Cloud Architecture & AI"</span><span class="ide-operator">,</span>
    <span class="ide-property">skills</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span><span class="ide-string">"AWS"</span><span class="ide-operator">,</span> <span class="ide-string">"Docker"</span><span class="ide-operator">,</span> <span class="ide-string">"Machine Learning"</span><span class="ide-operator">,</span> <span class="ide-string">"System Design"</span><span class="ide-bracket">]</span>
  <span class="ide-bracket">}</span>
<span class="ide-bracket">]</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Looking</span> <span class="ide-class">Forward</span>

<span class="ide-comment">// Future goals and planned milestones</span>

<span class="ide-keyword">const</span> <span class="ide-variable">upcomingGoals</span> <span class="ide-operator">=</span> <span class="ide-bracket">[</span>
  <span class="ide-string">"Launch AI-powered developer tools startup"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Speak at major tech conferences"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Contribute to open source projects"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Complete AWS Solutions Architect Professional"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Mentor 10+ developers through career transitions"</span>
<span class="ide-bracket">]</span><span class="ide-operator">;</span>

<span class="ide-comment">// Every milestone is a stepping stone to the next achievement</span>

<style>
.timeline-container {
  margin: 30px 0;
}

.timeline-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 20px;
  margin: 30px 0;
}

.stat-item {
  text-align: center;
  padding: 20px;
  border: var(--border);
  border-radius: 5px;
  background-color: rgba(255, 255, 255, 0.05);
}

.stat-value {
  font-size: 2em;
  font-weight: bold;
  color: var(--ide-function);
  margin-bottom: 5px;
}

.stat-label {
  font-size: 0.9em;
  color: var(--ide-comment);
}

.timeline-achievements {
  margin: 10px 0;
}

.timeline-achievements ul {
  margin: 5px 0;
  padding-left: 20px;
}

.timeline-achievements li {
  font-size: 0.9em;
  color: var(--text-color);
  margin-bottom: 3px;
}

.timeline-impact {
  margin: 10px 0;
  padding: 8px 12px;
  background-color: rgba(255, 215, 0, 0.1);
  border-left: 3px solid var(--ide-function);
  border-radius: 3px;
}

.timeline-impact .ide-function {
  font-weight: 500;
}

.timeline-action {
  margin-top: 10px;
}

@media (max-width: 768px) {
  .timeline-stats {
    grid-template-columns: repeat(2, 1fr);
  }
}
</style>
