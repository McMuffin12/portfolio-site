---
title: /contact
layout: page
permalink: /contact/
---

# <span class="ide-keyword">Get</span> <span class="ide-keyword">In</span> <span class="ide-class">Touch</span>

<span class="ide-comment">// Let's connect and build something amazing together</span>

<span class="ide-keyword">const</span> <span class="ide-variable">contact</span> <span class="ide-operator">=</span> <span class="ide-bracket">{</span>
  <span class="ide-property">status</span><span class="ide-operator">:</span> <span class="ide-string">"Available for freelance projects"</span><span class="ide-operator">,</span>
  <span class="ide-property">response_time</span><span class="ide-operator">:</span> <span class="ide-string">"Within 24 hours"</span><span class="ide-operator">,</span>
  <span class="ide-property">preferred_method</span><span class="ide-operator">:</span> <span class="ide-string">"Email"</span>
<span class="ide-bracket">}</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Contact</span> <span class="ide-class">Form</span>

<form id="contact-form" class="contact-form">
  <div class="form-group">
    <label for="name"><span class="ide-property">name</span><span class="ide-operator">:</span></label>
    <input type="text" id="name" name="name" placeholder="Your Name" required>
  </div>
  
  <div class="form-group">
    <label for="email"><span class="ide-property">email</span><span class="ide-operator">:</span></label>
    <input type="email" id="email" name="email" placeholder="your.email@example.com" required>
  </div>
  
  <div class="form-group">
    <label for="subject"><span class="ide-property">subject</span><span class="ide-operator">:</span></label>
    <input type="text" id="subject" name="subject" placeholder="Project Inquiry" required>
  </div>
  
  <div class="form-group">
    <label for="message"><span class="ide-property">message</span><span class="ide-operator">:</span></label>
    <textarea id="message" name="message" rows="6" placeholder="Tell me about your project..." required></textarea>
  </div>
  
  <button type="submit">
    <span class="ide-function">sendMessage</span><span class="ide-bracket">()</span>
  </button>
</form>

## <span class="ide-keyword">Other</span> <span class="ide-class">Ways</span> <span class="ide-keyword">to</span> <span class="ide-class">Connect</span>

<span class="ide-keyword">const</span> <span class="ide-variable">socialLinks</span> <span class="ide-operator">=</span> <span class="ide-bracket">{</span>
  <span class="ide-property">email</span><span class="ide-operator">:</span> <span class="ide-string">"your-email@example.com"</span><span class="ide-operator">,</span>
  <span class="ide-property">github</span><span class="ide-operator">:</span> <span class="ide-string">"github.com/yourusername"</span><span class="ide-operator">,</span>
  <span class="ide-property">linkedin</span><span class="ide-operator">:</span> <span class="ide-string">"linkedin.com/in/yourprofile"</span><span class="ide-operator">,</span>
  <span class="ide-property">twitter</span><span class="ide-operator">:</span> <span class="ide-string">"twitter.com/yourusername"</span><span class="ide-operator">,</span>
  <span class="ide-property">discord</span><span class="ide-operator">:</span> <span class="ide-string">"YourUsername#1234"</span>
<span class="ide-bracket">}</span><span class="ide-operator">;</span>

<div class="social-links">
  <a href="mailto:your-email@example.com" class="social-link">
    <span class="ide-property">email</span><span class="ide-operator">.</span><span class="ide-function">send</span><span class="ide-bracket">()</span>
  </a>
  <a href="https://github.com/yourusername" target="_blank" class="social-link">
    <span class="ide-property">github</span><span class="ide-operator">.</span><span class="ide-function">follow</span><span class="ide-bracket">()</span>
  </a>
  <a href="https://linkedin.com/in/yourprofile" target="_blank" class="social-link">
    <span class="ide-property">linkedin</span><span class="ide-operator">.</span><span class="ide-function">connect</span><span class="ide-bracket">()</span>
  </a>
  <a href="https://twitter.com/yourusername" target="_blank" class="social-link">
    <span class="ide-property">twitter</span><span class="ide-operator">.</span><span class="ide-function">follow</span><span class="ide-bracket">()</span>
  </a>
</div>

## <span class="ide-keyword">What</span> <span class="ide-class">I</span> <span class="ide-class">Can</span> <span class="ide-class">Help</span> <span class="ide-class">With</span>

<span class="ide-keyword">const</span> <span class="ide-variable">services</span> <span class="ide-operator">=</span> <span class="ide-bracket">[</span>
  <span class="ide-string">"Full-stack web application development"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Frontend development with React/Vue.js"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Backend API development with Node.js/Python"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Database design and optimization"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Code review and technical consulting"</span><span class="ide-operator">,</span>
  <span class="ide-string">"DevOps and deployment automation"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Performance optimization"</span><span class="ide-operator">,</span>
  <span class="ide-string">"Technical writing and documentation"</span>
<span class="ide-bracket">]</span><span class="ide-operator">;</span>

## <span class="ide-keyword">Response</span> <span class="ide-class">Time</span>

<span class="ide-keyword">const</span> <span class="ide-variable">responseTime</span> <span class="ide-operator">=</span> <span class="ide-bracket">{</span>
  <span class="ide-property">email</span><span class="ide-operator">:</span> <span class="ide-string">"Within 24 hours"</span><span class="ide-operator">,</span>
  <span class="ide-property">linkedin</span><span class="ide-operator">:</span> <span class="ide-string">"Within 48 hours"</span><span class="ide-operator">,</span>
  <span class="ide-property">twitter</span><span class="ide-operator">:</span> <span class="ide-string">"Within a few hours"</span><span class="ide-operator">,</span>
  <span class="ide-property">urgent</span><span class="ide-operator">:</span> <span class="ide-string">"Use email with [URGENT] in subject"</span>
<span class="ide-bracket">}</span><span class="ide-operator">;</span>

<span class="ide-comment">// Looking forward to hearing from you!</span>
<span class="ide-keyword">console</span><span class="ide-operator">.</span><span class="ide-function">log</span><span class="ide-bracket">(</span><span class="ide-string">"Ready to bring your ideas to life 🚀"</span><span class="ide-bracket">)</span><span class="ide-operator">;</span>
