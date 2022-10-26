---
layout: page
title: Projects
permalink: /projects/
---

{% for repo in site.github.public_repositories %}
{% if repo.fork == false and repo.topics.size > 0 %}



## [{{ repo.name }}]({{ repo.html_url }})

{{repo.description}}

Topics: {{ repo.topics | array_to_sentence_string}}

Last updated: {{repo.updated_at | date_to_string}}

{% endif %}

#review this webpage: https://henriwoodcock.medium.com/how-to-create-a-projects-page-on-jekyll-3bcf129f3efd
{% endfor %}
