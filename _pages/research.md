---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
header:
  og_image: "research/ecdf.png"
---
Albert Szent-Gyorgyi, a Nobel laureate and renowned scientist, famously remarked, “Research is to see what everybody else has seen, and to think what nobody else has thought.” Inspired by this perspective, my research focuses on uncovering novel insights and innovative solutions to critically challenged and widely recognized problems in software engineering. Specifically, I am dedicated to advancing the productivity of software practitioners through the automation of various software development tasks. One aspect of my research revolves around developing methodologies and tools that harness software artifacts, data analytics and AI to support various software maintenance processes – such as recommending appropriate code reviewers and predicting defect-prone modules – thereby alleviating the workload of practitioners and improving overall software quality. Through the integration of advanced machine learning techniques, natural language processing (NLP), and rigorous empirical analysis of large-scale data and mining software repositories, I aim to address critical challenges in developer engagement, software quality assurance, issue management, and empirical ecosystem analysis.

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
