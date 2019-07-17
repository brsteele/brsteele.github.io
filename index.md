---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: home
---

<div>
  {% for post in site.posts %}
    <div>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <div class="postInfoWrapper">
        <p>{{post.date | date: '%B %d, %Y'}}</p>
        <p>Tags: {% for tag in post.tags %}<a href="{{site.baseurl}}">{{tag}}</a>{% endfor%}</p>
      </div>
      <p>{{ post.excerpt }}</p>
    </div>
  {% endfor %}
</div>
