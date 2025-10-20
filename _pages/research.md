---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
header:
  og_image: "research/ecdf.png"
---

<div style="text-align: justify;">
Albert Szent-Gyorgyi, a Nobel laureate and renowned scientist, famously remarked, “Research is to see what everybody else has seen, and to think what nobody else has thought.” Inspired by this perspective, my research focuses on uncovering novel insights and innovative solutions to critically challenged and widely recognized problems in software engineering. Specifically, I am dedicated to advancing the productivity of software practitioners through the automation of various software development tasks. One aspect of my research revolves around developing methodologies and tools that harness software artifacts, data analytics and AI to support various software maintenance processes – such as recommending appropriate code reviewers and predicting defect-prone modules – thereby alleviating the workload of practitioners and improving overall software quality. Through the integration of advanced machine learning techniques, natural language processing (NLP), and rigorous empirical analysis of large-scale data and mining software repositories, I aim to address critical challenges in developer engagement, software quality assurance, issue management, and empirical ecosystem analysis.

My broad research works can be categorized into these three following areas:
</div>

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}

<div class="research-three-col">
  {% for post in ordered_pages %}
    <div class="research-card">
      {% include archive-single.html type="grid" %}
    </div>
  {% endfor %}
</div>

<style>
.research-three-col {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
}
.research-card {
  border: 1px solid #eee;
  padding: 10px;
  border-radius: 8px;
  background-color: #fff;
}
</style>