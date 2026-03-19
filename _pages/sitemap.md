---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: true
---

{% include base_path %}

A list of all the posts and pages found on the site. For you robots out there, there is an [XML version]({{ base_path }}/sitemap.xml) available for digesting as well.

<h2>Main Pages</h2>
{% for nav_item in site.data.navigation.main %}
  {% for page_item in site.pages %}
    {% if page_item.permalink == nav_item.url and page_item.sitemap != false and page_item.title %}
      {% assign post = page_item %}
      {% include archive-single.html %}
    {% endif %}
  {% endfor %}
{% endfor %}

<h2>Teaching</h2>
{% for post in site.teaching %}
  {% if post.sitemap != false and post.title %}
    {% unless post.title contains "[" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endif %}
{% endfor %}

<h2>Publications</h2>
{% for post in site.publications %}
  {% if post.sitemap != false and post.title %}
    {% unless post.title contains "[" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endif %}
{% endfor %}

<h2>Services &amp; Awards</h2>
{% for post in site.services %}
  {% if post.sitemap != false and post.title %}
    {% unless post.title contains "[" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endif %}
{% endfor %}
