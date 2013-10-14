---
layout: default
---

<style>
  .head {
    border-top: solid 1px #ccc;
    border-bottom: solid 1px #ccc;
    padding: 20px 0;
    background: hsl(200, 30%, 30%);
    color: white;
  }
</style>


<div class="head">
  <div class="kicker">Kevin and Shan’s</div>
  <h1 class="title">Field Guide to Working with Data in the Wild</h1>
</div>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }} - {{post.language}}</a>
      <p>{{ post.excerpt }}</p>
    </li>
  {% endfor %}
</ul>
