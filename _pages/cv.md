---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

{% assign journal_posts = site.publications | where: "category", "manuscripts" %}
{% assign journal_posts_with_order = journal_posts | where_exp: "item", "item.order" | sort: "order" %}
{% assign journal_posts_without_order = journal_posts | where_exp: "item", "item.order == nil" | sort: "date" | reverse %}
{% assign journal_post_list = journal_posts_with_order | concat: journal_posts_without_order %}

{% assign conference_posts = site.publications | where: "category", "conferences" %}
{% assign conference_posts_with_order = conference_posts | where_exp: "item", "item.order" | sort: "order" %}
{% assign conference_posts_without_order = conference_posts | where_exp: "item", "item.order == nil" | sort: "date" | reverse %}
{% assign conference_post_list = conference_posts_with_order | concat: conference_posts_without_order %}

Education
======
* Ph.D in Version Control Theory, GitHub University, 2018 (expected)
* M.S. in Jekyll, GitHub University, 2014
* B.S. in GitHub, GitHub University, 2012

Work experience
======
* Spring 2024: Academic Pages Collaborator
  * GitHub University
  * Duties includes: Updates and improvements to template
  * Supervisor: The Users

* Fall 2015: Research Assistant
  * GitHub University
  * Duties included: Merging pull requests
  * Supervisor: Professor Hub

* Summer 2015: Research Assistant
  * GitHub University
  * Duties included: Tagging issues
  * Supervisor: Professor Git
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
Journal Articles
------
  <ul>{% for post in journal_post_list %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>

Conference Papers
------
  <ul>{% for post in conference_post_list %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams
