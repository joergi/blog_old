
<ul>
  {% for post in site.posts %}
    <li>
      <div><a href="{{ post.url }}">{{ post.title }}</a></div>
      <div><time pubdate="">{{ post.date | date: "%B %-d, %Y" }}</time></div>
    </li>
  {% endfor %}
</ul>
