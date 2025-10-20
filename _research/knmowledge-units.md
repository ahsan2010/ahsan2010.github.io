---
title: "Knowledge Units of Programming Languages -- A new perspective for analyzing software systems"
layout: single-portfolio
excerpt: "<img src='/images/research/ku.png' alt=''>"
collection: research
order_number: 10
header: 
  og_image: "research/ku.png"
---

<div align="justify">

During my PhD I introduce the notion of Knowledge Units (KUs) - cohesive sets of key capabilities that are offered by one or more building blocks of a programming language. Unlike traditional code metrics such as lines of code, cyclomatic complexity, and the CK suite) that only offer language-agnostic insights into size, complexity, and structure, KUs aim to capture language-specific traits that influence how software systems are developed and maintained. For instance, using the Java language’s concurrency constructs and Application Programming Interfaces (APIs), a developer can create worker threads to execute tasks concurrently. Therefore, it is reasonable to assume that Java has a Concurrency KU, which includes a cohesive set of key concurrent processing capabilities offered by the Java Concurrency constructs/APIs (building block). 

<br>

Based on the assumption that expert programmers should master the KUs required for the development
task at hand, in my PhD, I conceptualize and operationalize KUs of programming languages and enhance various important software engineering tasks by leveraging KUs. In particular, I explore
KUs along four perspectives:

</div>
---

### 🧩 1. Recommending Code Reviewers in Pull Requests — *KUREC Framework*
- Developed **KUREC**, an effective reviewer recommender system that analyzes developers’ programming language expertise in both code contributions and prior reviews through the lens of KUs.  
- Evaluated KUREC on **10 large-scale Java projects** (290K commits and 65K PRs) from GitHub.  
- KUREC **outperforms seven state-of-the-art recommenders** and shows stable, reliable performance across projects.  
- Enhanced KUREC by integrating it with other recommenders and developing three new variations that further **balance reviewer workload** while maintaining high accuracy.  
- Published in *Empirical Software Engineering (EMSE)*, the top journal in empirical software research.

---

### 👥 2. Predicting Long-Time Contributors (LTCs) in OSS Projects — *KULTC Model*
- Proposed **KULTC**, a prediction model that leverages KU-based features along five distinct dimensions to identify long-time contributors in open-source software (OSS) projects.  
- Analyzed **1.7M commits and 168K PRs** from **4.3K active Java projects** to detect and quantify KUs.  
- Empirical results show that KULTC **outperforms baseline models** and effectively predicts LTCs during their early involvement in projects.  
- Local interpretability analysis revealed that **KU-based expertise is the most influential factor** in predicting long-term engagement.  
- Published in *Empirical Software Engineering (EMSE)*.

---

### 🐞 3. Predicting Post-Release Defects — *KUM Model*
- Designed **KUM**, a defect prediction model using **28 KU-based features**, providing a language-aware approach to software quality prediction.  
- Demonstrated that KUs offer **significant predictive power**, outperforming traditional metric groups (product, process, and ownership metrics).  
- Found that KUs offer a **complementary perspective** to existing metrics, improving both recall and interpretability in defect prediction.  
- This article is **currently under review** in *Empirical Software Engineering (EMSE)*.

---

### 🤖 4. Evaluating Large Language Models (LLMs) through KUs
- Addressed the gap in benchmark datasets (e.g., *HumanEval*, *MBPP*) which often lack equitable coverage of programming-language KUs.  
- Developed an **LLM-based framework** that:
  - Automatically detects KUs in any programming language,  
  - Generates **KU-specific code generation tasks** to enhance benchmark coverage, and  
  - Evaluates **LLMs’ strengths and weaknesses** across specific KUs.  
- Comparative analysis on real-world projects and benchmark datasets demonstrates **improved representativeness and coverage** in LLM evaluation.  
- This work is being finalized for submission to *IEEE Transactions on Software Engineering (TSE)*, the #1 journal in the software engineering field.

---

## Article

Ahasanuzzaman, M., Oliva, G. A., & Hassan, A. E. (2024). **Using knowledge units of programming languages to recommend reviewers for pull requests: an empirical study**. Empirical Software Engineering (EMSE), 29(1), 33.

>Code review is a key element of quality assurance in software development. Determining the right reviewer for a given code change requires understanding the characteristics of the changed code, identifying the skills of each potential reviewer (expertise profile), and finding a good match between the two. To facilitate this task, we design a code reviewer recommender that operates on the Knowledge Units (KUs) of a programming language. We define a KU as a cohesive set of key capabilities that are offered by one or more building blocks of a given programming language. We operationalize our KUs using certification exams for the Java programming language. We detect KUs from ten actively maintained Java projects from GitHub, spanning 290K commits and 65K pull requests (PRs). Next, we generate developer expertise profiles based on the detected KUs. Finally, these KU-based expertise profiles are used to build a code reviewer recommender (KUREC). The key assumption of KUREC is that the code reviewers of a given PR should be experts in the KUs that appear in the changed files of that PR. In RQ1, we compare KUREC’s performance to that of four baseline recommenders: (i) a commit-frequency-based recommender (CF), (ii) a review-frequency-based recommender (RF), (iii) a modification-expertise-based recommender (ER), and (iv) a review-history-based recommender (CHREV). We observe that KUREC performs as well as the top-performing baseline recommender (RF). From a practical standpoint, we highlight that KUREC’s performance is more stable (lower interquartile range) than that of RF, thus making it more consistent and potentially more trustworthy. Next, in RQ2, we design three new recommenders by combining KUREC with our baseline recommenders. These new combined recommenders outperform both KUREC and the individual baselines. Finally, in RQ3, we evaluate how reasonable the recommendations from KUREC and the combined recommenders are when those deviate from the ground truth. KUREC is the recommender with the highest percentage of reasonable recommendations (63.4%). One of our combined recommenders (AD_FREQ) strikes the best balance between sticking to the ground truth (best recommender from RQ2) and issuing reasonable recommendations when those deviate from that ground truth (59.4% reasonable recommendations, third best in this RQ). Taken together, the results from all RQs show that KUREC and AD_FREQ are overall superior to the baseline recommenders that we studied. Future work in this area should therefore (i) consider KU-based recommenders as baselines and (ii) experiment with combined recommenders.

[Article](https://link.springer.com/article/10.1007/s10664-023-10421-9){: .btn--research} [Preprint](https://arxiv.org/pdf/2305.05654){: .btn--research} [Supplemental Information](/files/pdf/research/Turning the Lights on SI.pdf){: .btn--research} [Replication Archive](https://drive.google.com/drive/folders/1bSC9iRtjKjMTRa9hiyECijgABKGfpyT4){: .btn--research}

## Article

Ahasanuzzaman, M., Oliva, G. A., & Hassan, A. E. (2025). **Predicting long time contributors with knowledge units of programming languages: an empirical study**. Empirical Software Engineering, 30(3), 99.

> Secessionist conflicts are likely to begin in specific types of places: those with abundant resources located far from the centers of state power. These factors affect the likelihood of secessionist conflict because dissidents will only rebel when they expect to be able to form a functional state within the borders of their territory following independence. There is a strong link between oil and secessionist conflict, but oil is far from the only resource a state can rely on. There are many regions that meet the necessary conditions for sovereign governance in the world, but few secessionist conflicts. I argue that this relative paucity of secessionist violence is the result of government preemption of potential secessionist movements. What strategies do governments use to try and preempt secession attempts by aggrieved minorities? What determines when they prefer to employ carrots vs sticks? Finally, what explains why these efforts break down allowing the onset of secessionist conflict? I argue that when discontinuous shifts in the resources available to ethnic groups within territories occur and governments' capabilities to monitor those territories prevent them from quickly updating their information, dissidents capitalize on this private information and initiate conflict. I investigate these dynamics with an agent based model of government surveillance and preemption strategies, studying the effect of exogenous shocks on resources within ethnic group territories on the likelihood of conflict onset. By varying how quickly the government is able to update its information in response to changes in ethnic group territories, I model the effect of government intelligence quality on the likelihood of conflict. These insights are combined with qualitative case study evidence to illustrate how failure in government preemption strategies can lead to secessionist conflict.

[Article](https://link.springer.com/article/10.1007/s10664-025-10655-9){: .btn--research} [Preprint](https://arxiv.org/pdf/2405.13852){: .btn--research} [Supplemental Information](/files/txt/Predicting%20Long%20Time%20Contributor.txt){: .btn--research} [Replication Archive](https://drive.google.com/drive/folders/1uaN8IUjrkhxcAT0lTyJbo_d72CB7hs1F){: .btn--research}


## Manuscript Under review

Ahasanuzzaman, M., Oliva, G. A., Hassan, A. E., & Ming, Z. (2024). **Predicting post-release defects with knowledge units (KUs) of programming languages: an empirical study**. arXiv preprint arXiv:2412.02907.

>Defect prediction plays a crucial role in software engineering, enabling developers to identify defect-prone code and improve software quality. While extensive research has focused on refining machine learning models for defect prediction, the exploration of new data sources for feature engineering remains limited. Defect prediction models primarily rely on traditional metrics such as product, process, and code ownership metrics, which, while effective, do not capture language-specific traits that may influence defect proneness. To address this gap, we introduce Knowledge Units (KUs) of programming languages as a novel feature set for analyzing software systems and defect prediction. A KU is a cohesive set of key capabilities that are offered by one or more building blocks of a given programming language. We conduct an empirical study leveraging 28 KUs that are derived from Java certification exams and compare their effectiveness against traditional metrics in predicting post-release defects across 28 releases of 8 well-maintained Java software systems. Our results show that KUs provide significant predictive power, achieving a median AUC of 0.82, outperforming individual group of traditional metric-based models (e.g., process, product and ownership metrics). Among KU features, Method & Encapsulation, Inheritance, and Exception Handling emerge as the most influential predictors. Furthermore, combining KUs with traditional metrics enhances prediction performance, yielding a median AUC of 0.89. We also introduce a cost-effective model using only 10 features (5 KUs and 5 traditional metrics), which maintains strong predictive performance while reducing feature engineering costs. Our findings demonstrate the value of KUs in predicting post-release defects, offering a complementary perspective to traditional metrics. This study can be helpful to researchers who wish to analyze software systems from a perspective that is complementary to that of traditional metrics.

## Manuscript Under Preparation

Studying Code Generation Benchmarks using Knowledge Units (KUs) of Programming Languages – An Empirical Study

>Large Language Models (LLMs) such as LLaMA and StarCoder have achieved notable progress in code generation tasks, with benchmark datasets like HumanEval and MBPP serving as the primary means of evaluation. However, the effectiveness of these evaluations of LLMs depends on how comprehensively benchmarks capture the core code concepts (data type, concurrency, exception handling and database) of programming languages. If critical code concepts are missing or underrepresented in benchmarks, evaluations may result in an incomplete understanding of LLM capabilities, thereby hindering their iterative improvement. While prior work has primarily explored on generating new benchmarks, improving benchmarks with new test cases, and addressing issues such as data leakage as benchmark quality, little attention has been paid to the comprehensiveness of code concepts. In this paper, we present the first systematic study of code concepts in benchmarks through the lens of Knowledge Units (KUs) — structured representations of code concepts (e.g., Concurrency, Object-Oriented Programming, File Handling) where each KU groups together a cohesive set of key capabilities that are offered by one or more building blocks of programming languages. As a first study in this area, we analyze two widely used code generation benchmarks HumanEval and MBPP alongside 30 real-world Python projects to investigate KU coverage. Our findings reveal that only half of the identified 20 Python KUs are represented in each benchmark, while real-world projects employ all of them. Benchmarks are skewed toward fundamental and core KUs (e.g., Exception handling and string manipulation), whereas real-world projects exhibit balanced use of these KUs. This gap suggests that the studied benchmarks may not fully evaluate the ability of a model to generate code and underscore the need for designing KU-aware benchmark. To address this gap, we develop an LLM-based framework that automatically generates KU-specific tasks using real-world code as context. Applying this framework, we generate 440 new tasks across 11 underrepresented KUs and construct augmented benchmarks: Augmented-HumanEval and Augmented-MBPP. The augmented benchmarks improve the KU coverage which closely aligns with the
KU coverage of real-world projects. Evaluation of seven popular LLMs on these augmented benchmarks shows a consistent performance drop (12.54–44.82\%), underscoring the difficulty of generating correct code for advanced KUs and highlighting distinct KU-specific strengths and weaknesses across models. Our findings provide valuable insights for researchers and practitioners aiming to design more comprehensive benchmarks, evaluate LLM's performance more effectively, and better understand model capabilities through the lens of KUs, ultimately guiding the improvement of LLMs.
