---
layout: default
---

<style>
  h3 {
    font-size: 24px;
    line-height: 24px;
    font-weight: normal;
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
</style>


<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{site.baseurl}}/{{ post.url }}"><h3>{{ post.title }} — {{post.language}}</h3></a>
      <p>{{ post.content }}</p>
    </li>
  {% endfor %}
</ul>
