---
layout: post
title: sample SNV notebook
date: 2023-08-11
description: sample SNV jupyter notebook
tags: notebook code
categories: how-to
giscus_comments: true
related_posts: false
---

Here's one of Matin's jupyter notebooks as an example:


{::nomarkdown}
{% assign jupyter_path = "assets/jupyter/test.ipynb" | relative_url %}
{% capture notebook_exists %}{% file_exists assets/jupyter/test.ipynb %}{% endcapture %}
{% if notebook_exists == "true" %}
    {% jupyter_notebook jupyter_path %}
{% else %}
    <p>Sorry, the notebook you are looking for does not exist.</p>
{% endif %}
{:/nomarkdown}

Note that the jupyter notebook supports both light and dark themes.
