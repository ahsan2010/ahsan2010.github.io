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
  gap: 36px;
  max-width: 900px;
  margin: 0 auto;
  padding: 30px 0;
}

.research-item {
  display: flex;
  flex-direction: column;
  justify-content: center;   /* vertically center content */
  align-items: center;       /* horizontally center content */
  text-align: center;
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 12px;
  padding: 30px;
  box-shadow: 0 3px 8px rgba(0,0,0,0.1);
  min-height: 320px;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.research-item:hover {
  transform: translateY(-4px);
  box-shadow: 0 6px 14px rgba(0,0,0,0.15);
}

.research-item h2,
.research-item h3,
.research-item h4 {
  width: 100%;
  font-size: 1.25rem;
  line-height: 1.4;
  font-weight: 600;
  color: #222;
  text-align: center;
  word-wrap: break-word;
  overflow-wrap: break-word;
  margin-bottom: 15px;
}

.research-item img {
  max-width: 150px;
  height: auto;
  border-radius: 8px;
  margin: 10px 0 15px;
  display: block;
}

@media (max-width: 768px) {
  .research-item {
    padding: 20px;
    min-height: 280px;
  }
}
</style>