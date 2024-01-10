---
layout: page
permalink: /code/
title: code
description: In these repository you'll find some of the code we've developed to look into TikTok. We can't publish everything to not risk our analysis, but if you are interested in learning more, please get in contact.
nav: true
nav_order: 3
---

{% if site.data.repositories.github_repos %}
<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.html repository=repo %}
  {% endfor %}
</div>
{% endif %}
