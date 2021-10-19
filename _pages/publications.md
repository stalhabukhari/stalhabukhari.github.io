---
layout: archive
title: "Selected Papers"
permalink: /publications/
author_profile: true
---

Up-to-date list of publications is available at: [<img src="https://img.shields.io/badge/Google%20Scholar-%230077B5.svg?&style=for-the-badge&logo=google-scholar&logoColor=blue&color=white" />](https://scholar.google.com/citations?user=B-lOirkAAAAJ&hl=en)

{% include base_path %}

{% for post in site.publications reversed %}
  {% include research-paper.html %}
{% endfor %}
