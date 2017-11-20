Java.PS
=======

GitHub Pages for Java.PS

tags:
* [Android](tag/Android)
* [Java software](tag/Java-software)
* [maven](tag/maven)

{% assign category = site.my_categories | where: "slug", post.category %}
{% assign category = category[0] %}
{% if category %}
    {% capture category_content %}<a class="label" href="{{ category.url }}">{{ category.name }}</a>{% endcapture %}
{% endif %}

<p id="post-meta">{{ category_content }}</p>

