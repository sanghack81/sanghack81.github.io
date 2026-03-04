---
layout: page2
title: Publications
permalink: /publications/
---

## Research Overview
  
My research explores the intersection of **causal inference** and **machine learning** to build robust, explainable, and fair AI systems. Our work is frequently published in top AI/ML venues such as NeurIPS, ICML, AAAI, UAI, and AISTATS.

[[Google Scholar](https://scholar.google.com/citations?hl=en&user=hsxjzdkAAAAJ&view_op=list_works&sortby=pubdate)], 
[[Openreview Profile](https://openreview.net/profile?id=~Sanghack_Lee1)]



Our core research themes include:
<ul style="margin-bottom: 0;">
  <li style="margin-bottom: 0.1em;"><strong>Identifiability &amp; Transportability</strong> <span class="pub-tag tag-id">ID</span> <span class="pub-tag tag-tr">TR</span> : Generalizing causal effect estimations across heterogeneous environments.</li>
  <li style="margin-bottom: 0.1em;"><strong>Causal Decision-Making</strong> <span class="pub-tag tag-dm">DM</span> : Utilizing causality as a first principle to optimize actions under uncertainty.</li>
  <li style="margin-bottom: 0.1em;"><strong>Causal Machine Learning</strong> <span class="pub-tag tag-cml">CML</span> : Developing causal representation learning and causality-inspired AI models.</li>
  <li style="margin-bottom: 0.1em;"><strong>Causal Discovery</strong> <span class="pub-tag tag-cd">CD</span> <span class="pub-tag tag-rel">REL</span> : Recovering underlying causal graphs from complex, observational, or relational data.</li>
</ul>

<!--My collaborators and I have published papers in AI and ML conferences (e.g., UAI, NeurIPS, ICML, AAAI, AISTATS).
Within the scope of causal inference, we investigated the problem of **causal effect identifiability** <span class="pub-tag tag-id">ID</span> allowing causal inference engines to take more diverse sets of data. In parallel, we also studied on the identifiability problem for heterogeneous domains (similar to the underlying ideas of domain adaptation or transfer learning in ML) called **transportability** <span class="pub-tag tag-tr">TR</span>. We also pursue research on **decision-making** <span class="pub-tag tag-dm">DM</span> where causality serves as the first principle to solve the problem.
During my PhD study, I mostly spent time on understanding causal discovery from **relational data** <span class="pub-tag tag-rel">REL</span> such as relational conditional independence, relational Markov equivalence classes, relational causal discovery algorithms both theoretical and practical. Recently, I am interested in the intersection of causality and machine learning <span class="pub-tag tag-cml">CML</span> (e.g., causal representation learning) and <span class="pub-tag tag-cd">CD</span> causal discovery.
-->

<!--**Collaborators**: [Juan D. Correa](http://jdcorrea.me), [Aria Khademi](https://sites.psu.edu/khademi/), [Elias Bareinboim](https://causalai.net), [Vasant Honavar](https://faculty.ist.psu.edu/vhonavar/index.htm)
-->




<p style="margin-bottom:1.25cm;"></p>
<!--
### Working Topics
- Unit Selection Prediction
- Mitigating Popularity bias in Recommender Systems
- Counterfactual Recommender Systems
- Representation Learning for Temporal Causal Discovery 
- LLM-Guided Temporal Causal Discovery (Juhyeon+, _submitted_)
- Citation for Retrieval Augmented Generation (Juhyeon+, _submitted_)
- Representation Learning for Instrumental Variables (Jung Soo+, _submitted_)
- Regularized Synthetic Control (Yeodong, Jeongsup, Inwoo)
- Causality-inspired Domain Generalization (Dong Kyu, Inwoo)
- Sequential Adjustment Criterion (YJ, Minwoo)
-->


<div class="pub-filters">
  <button class="pub-filter-btn active" data-filter="ALL">All</button>
  <button class="pub-filter-btn" data-filter="ID">ID</button>
  <button class="pub-filter-btn" data-filter="TR">TR</button>
  <button class="pub-filter-btn" data-filter="DM">DM</button>
  <button class="pub-filter-btn" data-filter="REL">REL</button>
  <button class="pub-filter-btn" data-filter="CD">CD</button>
  <button class="pub-filter-btn" data-filter="CML">CML</button>
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
  const filterBtns = document.querySelectorAll('.pub-filter-btn');
  const tags = document.querySelectorAll('.pub-tag');
  const pubItems = new Set();
  
  tags.forEach(tag => {
    const container = tag.closest('p, li');
    if (container && tag.closest('.pub-filters') === null) {
        if (!container.textContent.includes("My research explores") && !container.textContent.includes("I am an Associate Professor")) {
            pubItems.add(container);
        }
    }
  });

  // Get all year headings (h4) to hide/show them
  const yearHeadings = document.querySelectorAll('h4, h3:nth-of-type(n+3)'); // h3 for "before 2020", "Workshops" etc. Maybe just specifically target the year headers. Let's find all headers after pub-filters.
  const allHeadings = Array.from(document.querySelectorAll('h3, h4')).filter(h => {
    // only keep headers that come after the filters div
    const filtersDiv = document.querySelector('.pub-filters');
    return h.compareDocumentPosition(filtersDiv) & Node.DOCUMENT_POSITION_PRECEDING;
  });

  filterBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      filterBtns.forEach(b => b.classList.remove('active'));
      btn.classList.add('active');

      const filter = btn.getAttribute('data-filter');

      // 1. Show/hide items
      pubItems.forEach(item => {
        if (filter === 'ALL') {
          item.style.display = '';
        } else {
          const itemTags = Array.from(item.querySelectorAll('.pub-tag')).map(t => t.innerText.trim());
          if (itemTags.includes(filter)) {
            item.style.display = '';
          } else {
            item.style.display = 'none';
          }
        }
      });

      // 2. Hide/show headings based on filter
      if (filter === 'ALL') {
         allHeadings.forEach(h => {
             h.style.display = '';
             // Also show the spacing divs right before them
             if (h.previousElementSibling && h.previousElementSibling.tagName === 'DIV' && h.previousElementSibling.style.marginTop) {
                 h.previousElementSibling.style.display = '';
             }
         });
      } else {
         allHeadings.forEach(h => {
             h.style.display = 'none';
             if (h.previousElementSibling && h.previousElementSibling.tagName === 'DIV' && h.previousElementSibling.style.marginTop) {
                 h.previousElementSibling.style.display = 'none';
             }
         });
      }
    });
  });
});
</script>

### Preprints

<span class="pub-tag tag-dm">DM</span>
 On Transportability for Structural Causal Bandits [\[preprint\]](http://arxiv.org/abs/2511.17953)<br>
Min Woo Park, **Sanghack Lee**<br>


<span class="pub-tag tag-cml">CML</span> Towards Causal Representation Learning with Observable Sources as Auxiliaries [\[preprint\]](https://arxiv.org/abs/2509.19058)<br>
Kwonho Kim, Heejeong Nam, Inwoo Hwang, **Sanghack Lee**\*<br>


<span class="pub-tag tag-dm">DM</span>
 An Introduction to Causal Reinforcement Learning [\[preprint\]](https://causalai.net/r65.pdf)<br>
Elias Bareinboim, Junzhe Zhang, **Sanghack Lee**<br>





<!--
Can We Utilize Pre-trained Language Models within Causal Discovery Algorithms? [\[arXiv\]](https://arxiv.org/abs/2311.11212)<br>
Chanhui Lee, Juhyeon Kim, Yongjun Jeong, Juhyun Lyu, Junghee Kim, Sangmin Lee, Sangjun Han, Hyeokjun Choe, Soyeon Park, Woohyung Lim, Sungbin Lim, **Sanghack Lee**<br>
-->

### Published Papers

\* for joint first authorship or corresponding author

<div style="margin-top: 1.25em;"></div>
#### 2026

<span class="pub-tag tag-dm">DM</span> Counterfactual Structural Causal Bandits<br>
Min Woo Park, **Sanghack Lee**\*<br>
ICLR 2026 (to appear)<br>


<span class="pub-tag tag-cml">CML</span> Mitigating Length Bias in RLHF through a Causal Lens [\[arXiv\]](https://arxiv.org/abs/2511.12573)<br>
Hyeonji Kim, Sujeong Oh, **Sanghack Lee**\*<br>
AAAI 2026<br>


<div style="margin-top: 1.25em;"></div>
#### 2025

<span class="pub-tag tag-dm">DM</span>
Structural Causal Bandits under Markov Equivalence [\[paper\]](https://causalai.net/r122.pdf)<br>
 Min Woo Park, Andy Arditi, Elias Bareinboim\*, **Sanghack Lee**\*<br>
NeurIPS 2025<br>


<span class="pub-tag tag-dm">DM</span>
Non-Stationary Structural Causal Bandits [\[paper\]](https://openreview.net/pdf?id=F4LhOqhxkk)<br>
Yeahoon Kwon,  Yesong Choe, Soungmin Park, Neil Dhir\*, **Sanghack Lee**\*<br>
NeurIPS 2025<br>





<span class="pub-tag tag-cml">CML</span> On Predicting Post-Click Conversion Rate via Counterfactual Inference [\[arXiv\]](https://arxiv.org/abs/2510.04816) <br>
Junhyung Ahn, **Sanghack Lee**\*<br>
ICDM 2025 (<font color="#e41a1c">Best Paper Award Finalist</font>)<br>

<span class="pub-tag tag-cml">CML</span> PEER pressure: Model-to-Model Regularization for Single Source Domain Generalization [\[paper\]](https://openaccess.thecvf.com/content/CVPR2025/papers/Cho_PEER_Pressure_Model-to-Model_Regularization_for_Single_Source_Domain_Generalization_CVPR_2025_paper.pdf)<br>
Dong Kyu Cho, Inwoo Hwang, **Sanghack Lee**\*<br>
CVPR 2025<br>

<div style="margin-top: 1.25em;"></div>
#### 2024

<span class="pub-tag tag-dm">DM</span>
 Toward a Complete Criterion for Value of Information in Insoluble Decision Problems [\[paper\]](https://openreview.net/pdf?id=0RUzRV05Jn)<br>
Ryan Carey, **Sanghack Lee**, Robin J. Evans<br>
Transactions on Machine Learning 2024<br>





<span class="pub-tag tag-id">ID</span> Complete Graphical Criterion for Sequential Covariate Adjustment in Causal Inference [\[paper\]](https://openreview.net/forum?id=6gIcnPvw2x&referrer=%5Bthe%20profile%20of%20Yonghan%20Jung%5D(%2Fprofile%3Fid%3D~Yonghan_Jung1)) <br> 
Yonghan Jung, Min Woo Park, **Sanghack Lee**\*<br> 
NeurIPS 2024<br> 

<span class="pub-tag tag-cd">CD</span>
<span class="pub-tag tag-dm">DM</span>
<span class="pub-tag tag-cml">CML</span> Fine-Grained Causal Dynamics Learning with Quantization for Improving Robustness in Reinforcement Learning [\[paper\]](https://openreview.net/pdf?id=mrd4e8ZJjm), [\[poster\]](assets/2024-ICML-CRL-poster.pdf) <br>
Inwoo Hwang, Yunhyeok Kwak, Suhyung Choi, Byoung-Tak Zhang\*, **Sanghack Lee**\*<br>
ICML 2024 <span style="font-size:16px;color:gray;">(previously, GenPlan workshop at NeurIPS 2023, SCIS workshop at ICML 2023)</span><br>

<span class="pub-tag tag-id">ID</span> On Positivity Condition for Causal Inference [\[paper\]](https://openreview.net/pdf?id=6D0nyemiWk), [\[poster\]](assets/2024-ICML-positivity-poster.pdf)<br>
Inwoo Hwang\*, Yesong Choe\*, Yeahoon Kwon,  **Sanghack Lee**\*<br>
ICML 2024 <span style="font-size:16px;color:gray;">(+ Causality workshop at UAI 2024)</span><br>


<span class="pub-tag tag-cd">CD</span>
<span class="pub-tag tag-dm">DM</span>
Efficient Monte Carlo Tree Search via On-the-Fly State-Conditioned Action Abstraction [\[paper\]](https://openreview.net/pdf?id=UvDsWevxUI)<br>
Yunhyeok Kwak\*, Inwoo Hwang\*, Dooyoung Kim, **Sanghack Lee**\*, Byoung-Tak Zhang\*<br>
UAI 2024, <font color="#e41a1c">Oral</font><br>

<span class="pub-tag tag-cd">CD</span> Causal Discovery with Deductive Reasoning: One Less Problem [\[paper\]](https://openreview.net/pdf?id=HmhAFOD1Bz), [\[poster\]](assets/2024-UAI-deduce-dep-poster.pdf)<br>
Jonghwan Kim, Inwoo Hwang, **Sanghack Lee**\*<br>
UAI 2024<br>

<span class="pub-tag tag-cd">CD</span> Filter, Rank, and Prune: Learning Linear Cyclic Gaussian Graphical Models [\[paper\]](https://proceedings.mlr.press/v238/yi24a/yi24a.pdf)<br>
Soheun Yi, **Sanghack Lee**\*<br>
AISTATS 2024<br>

<div style="margin-top: 1.25em;"></div>
#### 2023



<!--
<span class="pub-tag tag-ws">ws</span>
<span class="pub-tag tag-dm">DM</span> Quantized Local Independence Discovery for Fine-Grained Causal Dynamics Learning in Reinforcement Learning<br>
Inwoo Hwang, Yunhyeok Kwak, Suhyung Choi, Byoung-Tak Zhang, **Sanghack Lee**<br> 
GenPlan 2023: Seventh Workshop on Generalization in Planning at NeurIPS 2023 [\[paper\]](https://openreview.net/forum?id=4xGCYC4dFp)<br>


<span class="pub-tag tag-ws">ws</span>
<span class="pub-tag tag-dm">DM</span> Causal Dynamics Learning with Quantized Local Independence Discovery<br>
Inwoo Hwang, Yunhyeok Kwak, Suhyung Choi, Byoung-Tak Zhang, **Sanghack Lee**<br> 
The Second Workshop on Spurious Correlations, Invariance and Stability at ICML 2023 [\[paper\]](https://openreview.net/forum?id=BXiA1YuOb7)
<br>
-->


<span class="pub-tag tag-cd">CD</span>
<span class="pub-tag tag-cml">CML</span> On Discovery of Local Independence over Continuous Variables via Neural Contextual Decomposition [\[paper\]](https://openreview.net/forum?id=-aFd28Uy9td)<br>
Inwoo Hwang, Yunhyeok Kwak, Yeon-Ji Song, Byoung-Tak Zhang\*, **Sanghack Lee**\*<br> 
CLeaR 2023 <br>

<div style="margin-top: 1.25em;"></div>
#### 2022




<span class="pub-tag tag-tr">TR</span> Counterfactual Transportability: A Formal Approach [\[paper\]](https://proceedings.mlr.press/v162/correa22a.html)<br> Juan D. Correa, **Sanghack Lee** and Elias Bareinboim<br> ICML 2022<br> 


<div style="margin-top: 1.25em;"></div>
#### 2021

<span class="pub-tag tag-id">ID</span> Nested Counterfactual Identification from Arbitrary Surrogate Experiments [\[paper\]](https://arxiv.org/abs/2107.03190)<br> Juan D. Correa, **Sanghack Lee** and Elias Bareinboim<br> NeurIPS 2021<br> 


<span class="pub-tag tag-id">ID</span> Causal Identification with Matrix Equations [\[paper\]](https://causalai.net/r70.pdf)<br> **Sanghack Lee** and Elias Bareinboim<br>
NeurIPS 2021, <font color="#e41a1c">Oral</font><br> 


### Workshops



<span class="pub-tag tag-ws">ws</span> 
<span class="pub-tag tag-id">ID</span> 
<span class="pub-tag tag-cml">CML</span> Instrumental Variable Representation Learning under Confounded Covariates<br>
Jungsoo Kim, Kwonho Kim, Inwoo Hwang, **Sanghack Lee**\*<br>
NeurIPS 2025 Workshop: CauScien---Uncovering Causality in Science<br>

<span class="pub-tag tag-ws">ws</span> 
<span class="pub-tag tag-cml">CML</span>Towards Causal Representation Learning with Observable Sources as Auxiliaries<br>
Kwonho Kim, Heejeong Nam, Inwoo Hwang, **Sanghack Lee**\*<br>
ICML 2025 Workshop on Scaling Up Intervention Models &amp; UAI 2025 Workshop on Causal Abstractions and Representations<br>

<span class="pub-tag tag-ws">ws</span> 
<span class="pub-tag tag-ml">ML</span> Locality-aware Concept Bottleneck Model<br>
Sujin Jeon, Inwoo Hwang, **Sanghack Lee**\*, Byoung-Tak Zhang\*<br>
UniReps: 2nd Edition of the Workshop on Unifying Representations in Neural Models at NeurIPS 2024<br>

<!--
<span class="pub-tag tag-ws">ws</span> 
<span class="pub-tag tag-cd">CD</span> On Incorporating Prior Knowledge Extracted from Pre-trained Language Models into Causal Discovery<br>
Chanhui Lee\*, Juhyeon Kim\*, YongJun Jeong, Yeom Yoon Seok, Juhyun Lyu, Jung-Hee Kim, Sangmin Lee, Sangjun Han, Hyeokjun Choe, Soyeon Park, Woohyung Lim, Kyunghoon Bae, Sungbin Lim\*, **Sanghack Lee**\*<br>
First Workshop on Causality and Large Model at NeurIPS 2024<br>
-->

<span class="pub-tag tag-ws">ws</span>
<span class="pub-tag tag-cml">CML</span> Learning to ignore: Single Source Domain Generalization via Oracle Regularization [\[paper\]](https://openreview.net/forum?id=8btzvHmSfU)<br>
Dong Kyu Cho, **Sanghack Lee**\*<br>
Causal Representation Learning Workshop at NeurIPS 2023<br>

<!--
<span class="pub-tag tag-ws">ws</span>
<span class="pub-tag tag-cml">CML</span> Detecting Causality by Data Augmentation via Part-of-Speech tagging<br> Juhyeon Kim, Yesong Choe and **Sanghack Lee**<br> CASE Workshop at EMNLP 2022<br> 
-->


<span class="pub-tag tag-ws">ws</span>
<span class="pub-tag tag-cd">CD</span>
Partition-based Local Independence Discovery<br> Inwoo Hwang, Byoung-Tak Zhang, and **Sanghack Lee** <br> Causal Inference Challenges in Sequential Decision Making: Bridging Theory and Practice Worksop at NeurIPS 2021<br> 



<div style="margin-top: 1.25em;"></div>
### before 2020

<span class="pub-tag tag-dm">DM</span> Characterizing Optimal Mixed Policies: Where to Intervene and What to Observe [\[paper\]](/assets/r63-reprint.pdf), [\[slides\]](/assets/2020-neurips-presentation.pdf), [\[poster\]](/assets/2020-neurips-sanghack-poster.pdf)<br> **Sanghack Lee** and Elias Bareinboim<br> NeurIPS 2020<br> 


<span class="pub-tag tag-id">ID</span> Causal Effect Identifiability under Partial-Observability [\[paper\]](https://causalai.net/r58.pdf) <br> **Sanghack Lee**, and Elias Bareinboim<br> ICML 2020<br> 


<span class="pub-tag tag-tr">TR</span> General Transportability --- Synthesizing Experiments from Heterogeneous Domains [\[paper\]](https://aaai.org/ojs/index.php/AAAI/article/view/6582/6438)<br> **Sanghack Lee**, Juan D. Correa, and Elias Bareinboim<br> AAAI 2020<br> 

<span class="pub-tag tag-id">ID</span> Identifiability from a Combination of Observations and Experiments [\[paper\]](https://aaai.org/ojs/index.php/AAAI/article/view/7119/6973), [\[slides\]](/assets/AAAI2020-GID-key.pdf)<br> **Sanghack Lee**, Juan D. Correa, and Elias Bareinboim<br> AAAI 2020 <br> 


<span class="pub-tag tag-id">ID</span> General Identifiability with Arbitrary Surrogate Experiments [\[paper\]](https://causalai.net/r46.pdf) [\[errata\]](https://causalai.net/r46e.pdf) <br> **Sanghack Lee**, Juan D. Correa, and Elias Bareinboim<br> UAI 2019, <font color="#e41a1c">Best Paper Award</font> <br> 

<span class="pub-tag tag-cd">CD</span> <span class="pub-tag tag-rel">REL</span> Towards Robust Relational Causal Discovery [\[paper\]](http://auai.org/uai2019/proceedings/papers/127.pdf) <br> **Sanghack Lee** and Vasant Honavar <br> UAI 2019<br> 



<span class="pub-tag tag-dm">DM</span> Fairness in Algorithmic Decision Making: An Excursion Through the Lens of Causality [\[paper\]](https://arxiv.org/pdf/1903.11719.pdf)<br> Aria Khademi, **Sanghack Lee**, David Foley, and Vasant Honavar<br> WWW 2019<br> 

<span class="pub-tag tag-dm">DM</span> On Structural Causal Bandit with Non-manipulable Variables [\[paper\]](https://causalai.net/r40.pdf), [\[poster\]](/assets/AAAI2019_poster.pdf), [\[slides\]](/assets/AAAI2019_presentation.pdf)<br> **Sanghack Lee** and Elias Bareinboim <br> AAAI 2019, <font color="#e41a1c">Oral</font><br> 



<span class="pub-tag tag-dm">DM</span>  Structural Causal Bandits: Where to Intervene? [\[paper\]](https://causalai.net/r36.pdf), [\[code\]](https://github.com/sanghack81/SCMMAB-NIPS2018), [\[poster\]](/assets/nips2018-poster.pdf)<br> **Sanghack Lee** and Elias Bareinboim<br> NeurIPS 2018<br> 


<span class="pub-tag tag-cd">CD</span> <span class="pub-tag tag-cit">CIT</span> <span class="pub-tag tag-rel">REL</span> A Kernel Conditional Independence Test for Relational Data [\[code\]](https://github.com/sanghack81/KRCIT), [\[paper\]](/assets/krcit.pdf)<br> **Sanghack Lee** and Vasant Honavar<br> UAI 2017<br> 


<span class="pub-tag tag-cit">CIT</span> Self-Discrepancy Conditional Independence Test [\[code\]](https://github.com/sanghack81/SDCIT), [\[paper\]](/assets/SDCIT-edited.pdf)<br> **Sanghack Lee** and Vasant Honavar<br> UAI 2017<br> 

<span class="pub-tag tag-cd">CD</span> <span class="pub-tag tag-rel">REL</span> A Characterization of Markov Equivalence Classes for Relational Causal Model with Path Semantics [\[code\]](https://github.com/sanghack81/pyRCDs), [\[paper\]](/assets/UAI-2016-RpCD.pdf), [\[appendix\]](/assets/UAI-2016-RpCD-supp_fix_june_4.pdf)<br> **Sanghack Lee** and Vasant Honavar<br> UAI 2016, <font color="#e41a1c">Oral</font><br> 

<span class="pub-tag tag-cd">CD</span> <span class="pub-tag tag-rel">REL</span> On Learning Causal Models from Relational Data [\[code\]](https://github.com/sanghack81/rcd-light) [\[paper\]](https://www.aaai.org/ocs/index.php/AAAI/AAAI16/paper/view/11972/12089)<br> **Sanghack Lee** and Vasant Honavar<br> AAAI 2016, <font color="#e41a1c">Oral</font> <br> 


<span class="pub-tag tag-social">social</span> "Teens are from Mars, Adults are from Venus": Analyzing and Predicting Age Groups with Behavioral Characteristics in Instagram [\[paper\]](http://dl.acm.org/citation.cfm?id=2908160)<br> Kyungsik Han, **Sanghack Lee**, Jin Yea Jang, Yong Jung, and Dongwon Lee<br> WebSci 2016<br> 



<span class="pub-tag tag-ws">ws</span>
<span class="pub-tag tag-cd">CD</span> <span class="pub-tag tag-rel">REL</span> Lifted Representation of Relational Causal Models Revisited: Implications for Reasoning and Structure Learning [\[paper\]](http://dl.acm.org/citation.cfm?id=3020273)<br> **Sanghack Lee** and Vasant Honavar<br> UAI 2015 Workshop on Advances in Causal Inference<br> 


<span class="pub-tag tag-tr">TR</span>  Transportability from Multiple Environments with Limited Experiments [\[paper\]](https://ftp.cs.ucla.edu/pub/stat_ser/r419.pdf)<br> Elias Bareinboim\*, **Sanghack Lee**\*, Vasant Honavar, and Judea Pearl<br> NeurIPS 2013<br> 


<span class="pub-tag tag-tr">TR</span> Causal Transportability of Experiments on Controllable Subsets of Variables: z-Transportability [\[paper\]](http://dl.acm.org/citation.cfm?id=3023675)<br> **Sanghack Lee** and Vasant Honavar<br> UAI 2013<br> 


<span class="pub-tag tag-tr">TR</span> m-Transportability: Transportability of a Causal Effect from Multiple Environments<br> **Sanghack Lee** and Vasant Honavar<br> AAAI 2013<br>


<span class="pub-tag tag-ml">ML</span> Learning Classifiers from Distributional Data<br> Harris Lin\*, **Sanghack Lee**\*, Ngot Bui\*, and Vasant Honavar<br> IEEE International Congress on Big Data





<!-- - (pre-PhD) A New Polynimial Time Algorithm for Bayesian Network Structure Learning
In Proceedings of the Second International Conference on Advanced Data Mining and Applications (ADMA 2006). pp. 501-508. (LNAI 4093)
- (pre-PhD) Discovery of Hidden Similarity on Collaborative Filtering to Overcome Sparsity Problem
In Proceedings of the Seventh International Conference on Discovery Science (DS 2004). Padova, Italy. pp. 396-402. (LNAI 3245)
 -->
