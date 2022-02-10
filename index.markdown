---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

{% for post in site.posts %}

## [{{ post.title }}]({{ site.baseurl }}{{ post.url }})
  {{ post.author }} | {{ post.date | date: '%B %d, %Y' }} | <em>{{ post.categories | join: "</em> - <em>" }}</em>
  <hr>
{% endfor %}
