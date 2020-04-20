# my digital brain

<ul>
  {% for post in site.posts %}
    <li>
      <div><time pubdate="">{{ post.date | date: "%B %-d, %Y" }}</time></div>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
