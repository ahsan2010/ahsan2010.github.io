---
title: "Knowledge Units of Programming Languages"
layout: single-portfolio
excerpt: "<img src='/images/research/epr.png' alt=''>"
collection: research
order_number: 10
header: 
  og_image: "research/epr.png"
---

During my PhD I introduce the notion of Knowledge Units (KUs) - cohesive sets of key capabilities that are offered by one or more building blocks of a programming language. Unlike traditional code metrics such as lines of code, cyclomatic complexity, and the CK suite) that only offer language-agnostic insights into size, complexity, and structure, KUs aim to capture language-specific traits that influence how software systems are developed and maintained. For instance, using the Java language’s concurrency constructs and Application Programming Interfaces (APIs), a developer can create worker threads to execute tasks concurrently. Therefore, it is reasonable to assume that Java has a Concurrency KU, which includes a cohesive set of key concurrent processing capabilities offered by the Java Concurrency constructs/APIs (building block). 

Based on the assumption that expert programmers should master the KUs required for the development
task at hand, in my PhD, I conceptualize and operationalize KUs of programming languages and enhance various important software engineering tasks by leveraging KUs. In particular, I explore
KUs along four perspectives:

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

>Code review is a key element of quality assurance in software development. Determining the right reviewer for a given code change requires understanding the characteristics of the changed code, identifying the skills of each potential reviewer (expertise profile), and finding a good match between the two. To facilitate this task, we design a code reviewer recommender that operates on the Knowledge Units (KUs) of a programming language. We define a KU as a cohesive set of key capabilities that are offered by one or more building blocks of a given programming language. We operationalize our KUs using certification exams for the Java programming language.

We detect KUs from ten actively maintained Java projects from GitHub, spanning 290K commits and 65K pull requests (PRs). Next, we generate developer expertise profiles based on the detected KUs. Finally, these KU-based expertise profiles are used to build a code reviewer recommender (KUREC). The key assumption of KUREC is that the code reviewers of a given PR should be experts in the KUs that appear in the changed files of that PR.

In RQ1, we compare KUREC’s performance to that of four baseline recommenders: (i) a commit-frequency-based recommender (CF), (ii) a review-frequency-based recommender (RF), (iii) a modification-expertise-based recommender (ER), and (iv) a review-history-based recommender (CHREV). We observe that KUREC performs as well as the top-performing baseline recommender (RF). From a practical standpoint, we highlight that KUREC’s performance is more stable (lower interquartile range) than that of RF, thus making it more consistent and potentially more trustworthy.

Next, in RQ2, we design three new recommenders by combining KUREC with our baseline recommenders. These new combined recommenders outperform both KUREC and the individual baselines. Finally, in RQ3, we evaluate how reasonable the recommendations from KUREC and the combined recommenders are when those deviate from the ground truth. KUREC is the recommender with the highest percentage of reasonable recommendations (63.4%). One of our combined recommenders (AD_FREQ) strikes the best balance between sticking to the ground truth (best recommender from RQ2) and issuing reasonable recommendations when those deviate from that ground truth (59.4% reasonable recommendations, third best in this RQ).

Taken together, the results from all RQs show that KUREC and AD_FREQ are overall superior to the baseline recommenders that we studied. Future work in this area should therefore (i) consider KU-based recommenders as baselines and (ii) experiment with combined recommenders.

[Article](https://link.springer.com/article/10.1007/s10664-023-10421-9){: .btn--research} [Preprint](https://arxiv.org/pdf/2305.05654){: .btn--research} [Supplemental Information](/files/pdf/research/Turning the Lights on SI.pdf){: .btn--research} [Replication Archive](https://drive.google.com/drive/folders/1bSC9iRtjKjMTRa9hiyECijgABKGfpyT4){: .btn--research}

## Manuscript in preparation

Rob Williams. "Keeping a Lid on it: How Government efforts to Prevent Secession Attempts can Fail." Presented at the International Studies Association Annual Convention, Toronto, ON, March 2019.

> Secessionist conflicts are likely to begin in specific types of places: those with abundant resources located far from the centers of state power. These factors affect the likelihood of secessionist conflict because dissidents will only rebel when they expect to be able to form a functional state within the borders of their territory following independence. There is a strong link between oil and secessionist conflict, but oil is far from the only resource a state can rely on. There are many regions that meet the necessary conditions for sovereign governance in the world, but few secessionist conflicts. I argue that this relative paucity of secessionist violence is the result of government preemption of potential secessionist movements. What strategies do governments use to try and preempt secession attempts by aggrieved minorities? What determines when they prefer to employ carrots vs sticks? Finally, what explains why these efforts break down allowing the onset of secessionist conflict? I argue that when discontinuous shifts in the resources available to ethnic groups within territories occur and governments' capabilities to monitor those territories prevent them from quickly updating their information, dissidents capitalize on this private information and initiate conflict. I investigate these dynamics with an agent based model of government surveillance and preemption strategies, studying the effect of exogenous shocks on resources within ethnic group territories on the likelihood of conflict onset. By varying how quickly the government is able to update its information in response to changes in ethnic group territories, I model the effect of government intelligence quality on the likelihood of conflict. These insights are combined with qualitative case study evidence to illustrate how failure in government preemption strategies can lead to secessionist conflict.