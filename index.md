---
layout: default
---

<style>
  .head {
    padding: 30px 0;
    text-align: center;
    border-bottom: solid 1px #ddd;
    font-family: Georgia;
  }

  h1 {
    font-weight: normal;
    font-size: 40px;
    margin: 10px 0;
  }

  h3 {
    font-size: 24px;
    line-height: 24px;
    font-weight: normal;
  }

  .kicker {
    font-size: 16px;
    text-transform: uppercase;
  }

  ul {
    margin: 0;
    padding: 0;
  }

  li {
    border-bottom: solid 1px #ccc;
    padding-bottom: 20px;
    display: block;
  }

  pre {
    border-left: solid 6px #ddd;
    background-color: #f0f0f0;
    padding: 10px 10px 10px 20px;
  }
</style>


<div class="head">
  <div class="kicker">Kevin and Shan’s</div>
  <h1 class="title">Field Guide to Working with Data in the Wild</h1>
</div>

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}"><h3>{{ post.title }} ({{post.language}})</h3></a>
      <p>{{ post.content }}</p>
    </li>
  {% endfor %}
</ul>
