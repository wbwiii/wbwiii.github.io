---
layout: page
permalink: /repositories/
title: repositories
description: I work at the intersection of machine learning, applied physics and instrumentation building systems that connect real world measurements to computational models. My work spans intelligent sensing, data acquisition and analysis across domains including optical and quantum systems, nuclear and RF instrumentations and electro-mechanical sensing.I'm most interested in problems where theory meets hardware and the software must hold up outside the lab. That has led me to design end to end ML system, from experimental data and signal processing through modeling, evaluation and production deployment. I'm comfortable moving between the bench to the cloud and I value work that is both technically rigorous and practically grounded.I believe durable progress comes from building tools, systems and insititutions that is for the beneifit of all.  
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub users

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for user in site.data.repositories.github_users %}
    {% include repository/repo_user.liquid username=user %}
  {% endfor %}
</div>

---

{% if site.repo_trophies.enabled %}
{% for user in site.data.repositories.github_users %}
{% if site.data.repositories.github_users.size > 1 %}

  <h4>{{ user }}</h4>
  {% endif %}
  <div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo_trophies.liquid username=user %}
  </div>

---

{% endfor %}
{% endif %}
{% endif %}

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>
{% endif %}
