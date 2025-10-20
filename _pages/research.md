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

<br/>

**My research can be broadly categorized into the following areas. Select a topic below to explore each area in greater depth.**
</div>

<nbsp>

{% include base_path %}

{% assign ordered_pages = site.research | sort:"order_number" %}
{% assign research_items = ordered_pages | slice: 0, 3 %}

<div class="research-column">
  {% for post in research_items %}
    <div class="research-item">
      {% include archive-single.html type="grid" %}
    </div>
  {% endfor %}
</div>

<style>
.research-column {
  display: grid;
  grid-template-columns: 1fr;
  gap: 32px;
  max-width: 900px;
  margin: 0 auto;
  padding: 20px 0;
}

.research-item {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0 3px 8px rgba(0,0,0,0.1);
  overflow: hidden;
}

.research-item h2,
.research-item h3,
.research-item h4 {
  font-size: 1.2rem;
  line-height: 1.4;
  word-wrap: break-word;
  overflow-wrap: break-word;
  margin-bottom: 12px;
  text-align: center;
}

.research-item img {
  max-width: 100%;
  height: auto;
  border-radius: 6px;
  margin: 10px auto 15px;
  display: block;
}

@media (max-width: 768px) {
  .research-column {
    padding: 10px;
  }
  .research-item {
    padding: 15px;
  }
}
</style>