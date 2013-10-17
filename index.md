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

  input {
    width: 400px;
    font-size: 20px;
    line-height: 24px;
  }

</style>

<label>Search</label>
<input type="search"></input>

<ul>
  {% for post in site.posts %}
    <li data-title="{{ post.title }}" data-language="{{ post.language }}">
      <a href="{{ site.baseurl }}{{ post.url }}"><h3>{{ post.title }} — {{ post.language }}</h3></a>
      <p>{{ post.content }}</p>
    </li>
  {% endfor %}
</ul>


<script>
var snippetData = d3.selectAll("li"),
    search = d3.select("input");

search.on("change", function(){
  console.log(d3.event.target.value)
})
</script>
