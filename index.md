{% for post in site.posts %}
## [{{ post.title }}]({{ post.url }})
<small>Published on {{ post.date | date: "%B %-d, %Y" }}</small>

{{ post.excerpt }}

[Read more...]({{ post.url | prepend: site.baseurl }})

---

{% endfor %}
