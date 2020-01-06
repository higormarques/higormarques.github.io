---
layout: higormarques
title: Higor Marques - Blog
---

<ul class="posts__list">
  {% for post in site.posts %}
    <li class="posts__item">
        <a href="{{ post.url }}" class="posts__anchor">
            <h2 class="posts__title">{{ post.title }}</h2>
            <p class="posts__subtitle">{{ post.subtitle }}</p>
            <footer class="posts__footer">
                <ul class="posts__categories">
                    {% for category in post.categories %}
                        <li class="posts__categories-item category-label category-label--{{ category }}">
                            {{ category }}
                        </li>
                    {% endfor %}
                </ul>
                <span class="posts__custom-date">
                    {{ post.customDate }}
                </span>
            </footer>
        </a>
    </li>
  {% endfor %}
</ul>