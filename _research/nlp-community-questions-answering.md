---
title: "Enhancing API-related issue identification with an NLP-based approach"
layout: single-portfolio
excerpt: "<img src='/images/research/NLP-image-scaled-1-1.png' alt=''>"
collection: research
order_number: 30
header: 
  og_image: "research/NLP-image-scaled-1-1.png"
---

I collaborated with researchers in University of Saskatchewan, Canada. In particular,
I investigated how issues related to Application Programming Interfaces (APIs) are discussed in
Stack Overflow (SO) posts. SO Posts about API-related issues are valuable to API designers for
understanding problems and user requirements. However, their unstructured format and the presence
of many unrelated posts make identifying relevant issues challenging. By analyzing a large dataset
of Q&A posts, I identified linguistic and structural patterns that distinguish API issues from general
programming questions. Building on this, I developed a supervised NLP-based technique called
CAPS, which effectively classifies API-related issues. This work was published at the SANER
2018 conference (a major conference in the field of software engineering) and is recognized as one of
the most influential papers. I later extended this work. The extended version introduced a broader
taxonomy of API-related issues, enhanced feature engineering, and demonstrated significantly higher
classification performance across multiple API domains. The findings from this work can help tool
builders and API providers better detect, monitor, and respond to API-related issues raised by
developers in online community question and answering (CQA) sites.

## Article

Ahasanuzzaman, M., Asaduzzaman, M., Roy, C. K., & Schneider, K. A. (2020). **CAPS: a supervised technique for classifying Stack Overflow posts concerning API issues**. Empirical Software Engineering (EMSE), 25(2), 1493-1532.

> The design and maintenance of APIs (Application Programming Interfaces) are complex tasks due to the constantly changing requirements of their users. Despite the efforts of their designers, APIs may suffer from a number of issues (such as incomplete or erroneous documentation, poor performance, and backward incompatibility). To maintain a healthy client base, API designers must learn these issues to fix them. Question answering sites, such as Stack Overflow (SO), have become a popular place for discussing API issues. These posts about API issues are invaluable to API designers, not only because they can help to learn more about the problem but also because they can facilitate learning the requirements of API users. However, the unstructured nature of posts and the abundance of non-issue posts make the task of detecting SO posts concerning API issues difficult and challenging. In this paper, we first develop a supervised learning approach using a Conditional Random Field (CRF), a statistical modeling method, to identify API issue-related sentences. We use the above information together with different features collected from posts, the experience of users, readability metrics and centrality measures of collaboration network to build a technique, called CAPS, that can classify SO posts concerning API issues. In total, we consider 34 features along eight different dimensions. Evaluation of CAPS using carefully curated SO posts on three popular API types reveals that the technique outperforms all three baseline approaches we consider in this study. We then conduct studies to find important features and also evaluate the performance of the CRF-based technique for classifying issue sentences. Comparison with two other baseline approaches shows that the technique has high potential. We also test the generalizability of CAPS results, evaluate the effectiveness of different classifiers, and identify the impact of different feature sets.

[Article](https://link.springer.com/article/10.1007/s10664-019-09743-4){: .btn--research} [Preprint](https://www.researchgate.net/profile/Md-Ahasanuzzaman/publication/334575687_CAPS_a_supervised_technique_for_classifying_Stack_Overflow_posts_concerning_API_issues/links/5d4c43daa6fdcc370a871569/CAPS-a-supervised-technique-for-classifying-Stack-Overflow-posts-concerning-API-issues.pdf?_sg%5B0%5D=started_experiment_milestone&_sg%5B1%5D=started_experiment_milestone&origin=journalDetail){: .btn--research}

## Article

Ahasanuzzaman, M., Asaduzzaman, M., Roy, C. K., & Schneider, K. A. (2018, March). **Classifying stack overflow posts on API issues**. In 2018 IEEE 25th international conference on software analysis, evolution and reengineering (SANER) (pp. 244-254). IEEE.

> The design and maintenance of APIs are complex tasks due to the constantly changing requirements of its users. Despite the efforts of its designers, APIs may suffer from a number of issues (such as incomplete or erroneous documentation, poor performance, and backward incompatibility). To maintain a healthy client base, API designers must learn these issues to fix them. Question answering sites, such as Stack Overflow (SO), has become a popular place for discussing API issues. These posts about API issues are invaluable to API designers, not only because they can help to learn more about the problem but also because they can facilitate learning the requirements of API users. However, the unstructured nature of posts and the abundance of non-issue posts make the task of detecting SO posts concerning API issues difficult and challenging. In this paper, we first develop a supervised learning approach using a Conditional Random Field (CRF), a statistical modeling method, to identify API issue-related sentences. We use the above information together with different features of posts and experience of users to build a technique, called CAPS, that can classify SO posts concerning API issues. Evaluation of CAPS using carefully curated SO posts on three popular API types reveals that the technique outperforms all three baseline approaches we consider in this study. We also conduct studies to test the generalizability of CAPS results and to understand the effects of different sources of information on it.


## Article

Ahasanuzzaman, M., Asaduzzaman, M., Roy, C. K., & Schneider, K. A. (2016, May). **Mining duplicate questions in stack overflow**. In Proceedings of the 13th International Conference on Mining Software Repositories (pp. 402-412).

>Stack Overflow is a popular question answering site that is focused on programming problems. Despite efforts to prevent asking questions that have already been answered, the site contains duplicate questions. This may cause developers to unnecessarily wait for a question to be answered when it has already been asked and answered. The site currently depends on its moderators and users with high reputation to manually mark those questions as duplicates, which not only results in delayed responses but also requires additional efforts. In this paper, we first perform a manual investigation to understand why users submit duplicate questions in Stack Overflow. Based on our manual investigation we propose a classification technique that uses a number of carefully chosen features to identify duplicate questions. Evaluation using a large number of questions shows that our technique can detect duplicate questions with reasonable accuracy. We also compare our technique with DupPredictor, a state-of-the-art technique for detecting duplicate questions, and we found that our proposed technique has a better recall-rate than that technique.

[Article](https://dl.acm.org/doi/pdf/10.1145/2901739.2901770?casa_token=OO_rTObSfKQAAAAA:eqQVLrYc7713LxsuYN1QtuUHsBlBvaQNcPnoPb1xgZR5u_1yEWPu_XaQdSnhz8fRXBaZaTIlGefqRnQ){: .btn--research} 

## Article
Asaduzzaman, M., Ahasanuzzaman, M., Roy, C. K., & Schneider, K. A. (2016, May). **How developers use exception handling in Java?**. In Proceedings of the 13th International Conference on Mining Software Repositories (pp. 516-519).

>Exception handling is a technique that addresses exceptional conditions in applications, allowing the normal flow of execution to continue in the event of an exception and/or to report on such events. Although exception handling techniques, features and bad coding practices have been discussed both in developer communities and in the literature, there is a marked lack of empirical evidence on how developers use exception handling in practice. In this paper we use the Boa language and infrastructure to analyze 274k open source Java projects in GitHub to discover how developers use exception handling. We not only consider various exception handling features but also explore bad coding practices and their relation to the experience of developers. Our results provide some interesting insights. For example, we found that bad exception handling coding practices are common in open source Java projects and regardless of experience all developers use bad exception handling coding practices.

[Article](https://dl.acm.org/doi/pdf/10.1145/2901739.2903500?casa_token=2oLCYaDydSoAAAAA:uJ3ZqlugZH7pGjQhndbjRYrQhpk90x8PyXbrZTJRHrkEVa8tAuEzUK9ZVtKrBFvYBIUECBssQh1Zdac){: .btn--research} 