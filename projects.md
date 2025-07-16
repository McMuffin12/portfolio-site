---
title: /projects
layout: page
permalink: /projects/
---

# <span class="ide-keyword">Projects</span> <span class="ide-operator">&</span> <span class="ide-class">Portfolio</span>

<span class="ide-comment">// A collection of my favorite projects and contributions</span>

<span class="ide-keyword">const</span> <span class="ide-variable">projects</span> <span class="ide-operator">=</span> <span class="ide-bracket">[</span>
  <span class="ide-comment">// Featured projects with live demos and source code</span>
<span class="ide-bracket">]</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Featured</span> <span class="ide-class">Projects</span>

<div class="projects-grid">
  {% for project in site.projects %}
    <div class="project-card">
      <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
      <p class="project-meta">
        <span class="ide-property">Tech Stack:</span> 
        {% for tech in project.tech %}
          <span class="ide-string">{{ tech }}</span>{% unless forloop.last %}, {% endunless %}
        {% endfor %}
      </p>
      <p>{{ project.description }}</p>
      <div class="project-links">
        {% if project.demo_url %}
          <a href="{{ project.demo_url }}" target="_blank" class="demo-link">
            <span class="ide-function">liveDemo</span><span class="ide-bracket">()</span>
          </a>
        {% endif %}
        {% if project.github_url %}
          <a href="{{ project.github_url }}" target="_blank" class="github-link">
            <span class="ide-keyword">source</span><span class="ide-operator">.</span><span class="ide-property">code</span>
          </a>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>

## <span class="ide-keyword">Open</span> <span class="ide-class">Source</span> <span class="ide-class">Contributions</span>

<span class="ide-comment">// Some of my contributions to the open source community</span>

<span class="ide-keyword">const</span> <span class="ide-variable">contributions</span> <span class="ide-operator">=</span> <span class="ide-bracket">[</span>
  <span class="ide-bracket">{</span>
    <span class="ide-property">project</span><span class="ide-operator">:</span> <span class="ide-string">"React"</span><span class="ide-operator">,</span>
    <span class="ide-property">type</span><span class="ide-operator">:</span> <span class="ide-string">"Bug Fix"</span><span class="ide-operator">,</span>
    <span class="ide-property">description</span><span class="ide-operator">:</span> <span class="ide-string">"Fixed memory leak in useEffect hook"</span><span class="ide-operator">,</span>
    <span class="ide-property">pr</span><span class="ide-operator">:</span> <span class="ide-string">"#12345"</span>
  <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span>
    <span class="ide-property">project</span><span class="ide-operator">:</span> <span class="ide-string">"Node.js"</span><span class="ide-operator">,</span>
    <span class="ide-property">type</span><span class="ide-operator">:</span> <span class="ide-string">"Feature"</span><span class="ide-operator">,</span>
    <span class="ide-property">description</span><span class="ide-operator">:</span> <span class="ide-string">"Added support for async/await in modules"</span><span class="ide-operator">,</span>
    <span class="ide-property">pr</span><span class="ide-operator">:</span> <span class="ide-string">"#67890"</span>
  <span class="ide-bracket">}</span><span class="ide-operator">,</span>
  <span class="ide-bracket">{</span>
    <span class="ide-property">project</span><span class="ide-operator">:</span> <span class="ide-string">"TypeScript"</span><span class="ide-operator">,</span>
    <span class="ide-property">type</span><span class="ide-operator">:</span> <span class="ide-string">"Documentation"</span><span class="ide-operator">,</span>
    <span class="ide-property">description</span><span class="ide-operator">:</span> <span class="ide-string">"Improved generic types documentation"</span><span class="ide-operator">,</span>
    <span class="ide-property">pr</span><span class="ide-operator">:</span> <span class="ide-string">"#54321"</span>
  <span class="ide-bracket">}</span>
<span class="ide-bracket">]</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Technologies</span> <span class="ide-operator">&</span> <span class="ide-class">Tools</span>

<span class="ide-comment">// Technologies I work with regularly</span>

<span class="ide-keyword">const</span> <span class="ide-variable">techStack</span> <span class="ide-operator">=</span> <span class="ide-bracket">{</span>
  <span class="ide-property">frontend</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span>
    <span class="ide-string">"React"</span><span class="ide-operator">,</span> <span class="ide-string">"Vue.js"</span><span class="ide-operator">,</span> <span class="ide-string">"TypeScript"</span><span class="ide-operator">,</span> <span class="ide-string">"Next.js"</span><span class="ide-operator">,</span>
    <span class="ide-string">"Tailwind CSS"</span><span class="ide-operator">,</span> <span class="ide-string">"Styled Components"</span><span class="ide-operator">,</span> <span class="ide-string">"Framer Motion"</span>
  <span class="ide-bracket">]</span><span class="ide-operator">,</span>
  <span class="ide-property">backend</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span>
    <span class="ide-string">"Node.js"</span><span class="ide-operator">,</span> <span class="ide-string">"Express"</span><span class="ide-operator">,</span> <span class="ide-string">"Python"</span><span class="ide-operator">,</span> <span class="ide-string">"Django"</span><span class="ide-operator">,</span>
    <span class="ide-string">"GraphQL"</span><span class="ide-operator">,</span> <span class="ide-string">"REST APIs"</span><span class="ide-operator">,</span> <span class="ide-string">"Microservices"</span>
  <span class="ide-bracket">]</span><span class="ide-operator">,</span>
  <span class="ide-property">database</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span>
    <span class="ide-string">"PostgreSQL"</span><span class="ide-operator">,</span> <span class="ide-string">"MongoDB"</span><span class="ide-operator">,</span> <span class="ide-string">"Redis"</span><span class="ide-operator">,</span> <span class="ide-string">"Elasticsearch"</span>
  <span class="ide-bracket">]</span><span class="ide-operator">,</span>
  <span class="ide-property">devops</span><span class="ide-operator">:</span> <span class="ide-bracket">[</span>
    <span class="ide-string">"Docker"</span><span class="ide-operator">,</span> <span class="ide-string">"Kubernetes"</span><span class="ide-operator">,</span> <span class="ide-string">"AWS"</span><span class="ide-operator">,</span> <span class="ide-string">"CI/CD"</span><span class="ide-operator">,</span> <span class="ide-string">"Terraform"</span>
  <span class="ide-bracket">]</span>
<span class="ide-bracket">}</span><span class="ide-operator">;</span>

<span class="ide-comment">// Always experimenting with new technologies</span>
<span class="ide-keyword">console</span><span class="ide-operator">.</span><span class="ide-function">log</span><span class="ide-bracket">(</span><span class="ide-string">"Curious about a specific project? Let's talk!"</span><span class="ide-bracket">)</span><span class="ide-operator">;</span>
