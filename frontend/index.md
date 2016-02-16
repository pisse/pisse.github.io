---
 layout: default
 title:  "大前端"
 date:   2016-02-15 21:20:43 +0800
---

<ul class="post-list">
{% for post in site.categories.frontend %}
  <li>
    <article>
      <aside class="post-meta">
        <time>{{ post.date | date: "%b %-d, %Y" }}</time>
        <a href="">1 comments</a>
      </aside>

      <section class="content-wrap">
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        <p class="content">
          {{ post.excerpt | remove: '<p>' | remove: '</p>' }}
        </p>
      </section>
    </article>
  </li>
{% endfor %}
</ul>
