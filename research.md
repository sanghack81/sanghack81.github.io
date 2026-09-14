---
layout: page2
title: Research
permalink: /research/
---

<div class="research-overview" markdown="1">

## Research

How can we learn what causes what, and use that knowledge to make better decisions? At the Causality Lab, we connect mathematical questions about what can be learned with statistical methods and algorithms for learning it.

### Causal inference: identification and estimation

*What can the evidence tell us about an intervention, and how precisely?*

We study when causal effects and counterfactuals can be uniquely determined from the available data and assumptions, how to bound them when they cannot, and how to estimate them from finite samples. This includes [combining observations and experiments](https://causalai.net/r46.pdf), [transferring conclusions across settings](https://proceedings.mlr.press/v162/correa22a.html), and understanding which variables and data support are needed for valid inference. We also develop models for estimating outcome distributions under interventions over time.

- [Causal Identification with Matrix Equations](https://causalai.net/r70.pdf) · NeurIPS 2021, Oral
- [On Positivity Condition for Causal Inference](https://proceedings.mlr.press/v235/hwang24a.html) · ICML 2024
- [Complete Graphical Criterion for Sequential Covariate Adjustment in Causal Inference](https://proceedings.neurips.cc/paper_files/paper/2024/hash/233ff375b9795cd890f78a1f64459b8d-Abstract-Conference.html) · NeurIPS 2024
- [Canonical Domain Reduction for Partial Counterfactual Identification](/assets/2026-UAI-canonical-domain-reduction-paper.pdf) · UAI 2026
- [Estimating Interventional Outcomes over Time with Causal Normalizing Flow](/assets/2026-UAI-tscnf-paper.pdf) · UAI 2026

### Causal discovery

*Which causal structures can we learn from data?*

We develop statistical tests and algorithms for learning causal structure, including settings with feedback loops and relationships among multiple entities. The challenges are both statistical and computational: determining which structures the data can distinguish, and searching large spaces of possible graphs. Our approaches include constraint-based learning, score-based search, and logical reasoning. For example, our deduction-based methods use relationships already established by simpler tests to avoid some harder tests.

- [Filter, Rank, and Prune: Learning Linear Cyclic Gaussian Graphical Models](https://proceedings.mlr.press/v238/yi24a.html) · AISTATS 2024
- [Don't Test What You Can Deduce: Causal Discovery with Logical Inference](/assets/2026-UAI-dfpc-paper-2026-09-14.pdf) (revised version) · UAI 2026, Oral · [code](https://github.com/snu-causality-lab/DF-PC)
- [Breaking Bad: Component-Wise Parent Deletion for Score-Based Causal Discovery](/assets/2026-UAI-breaking-bad-paper.pdf) · UAI 2026

### Causal decision-making

*Where should we intervene, and what should we observe before acting?*

We use causal models to study how an agent should act and learn. This includes choosing which variables to control, which information a policy should use, and which interventions are worth exploring. Our work ranges from characterizing optimal policies to narrowing the action space when the causal structure is only partially known, and expanding it to include realizable counterfactual actions.

- [Characterizing Optimal Mixed Policies: Where to Intervene and What to Observe](/assets/r63-reprint.pdf) · NeurIPS 2020
- [Structural Causal Bandits under Markov Equivalence](https://causalai.net/r122.pdf) · NeurIPS 2025
- [Counterfactual Structural Causal Bandits](https://openreview.net/forum?id=gjvTNxVd2f) · ICLR 2026

### Causal machine learning

*How can causal structure improve what a model learns?*

We study how causal assumptions can guide representation learning, generative modeling, and generalization, and how they can help diagnose biases in learning systems. One line of work asks when hidden factors can be recovered from observations. Another examines what reward models actually reward: for example, whether a response receives a higher score because of its content or simply its length.

- [PEER Pressure: Model-to-Model Regularization for Single Source Domain Generalization](https://openaccess.thecvf.com/content/CVPR2025/papers/Cho_PEER_Pressure_Model-to-Model_Regularization_for_Single_Source_Domain_Generalization_CVPR_2025_paper.pdf) · CVPR 2025
- [Mitigating Length Bias in RLHF through a Causal Lens](https://ojs.aaai.org/index.php/AAAI/article/view/38806) · AAAI 2026
- [On Causal Representation Learning with Internal Auxiliaries](/assets/2026-UAI-crl-internal-auxiliaries-paper.pdf) · UAI 2026

[All publications](/publications/) · [Meet the lab](/members/)

If one of these questions interests you, [consider joining us](/join/). Prior experience in causal inference is not required.

</div>

<details markdown="1" style="margin-top:2.5rem;">
<summary style="cursor:pointer;">Funding &amp; collaborations</summary>

### Current projects

- Causal Machine Learning (NRF, PI, 2023 ~ 27 with Innovative Research Lab Initiation Grant)
- Self-Motivated AI: Developing self-directed AI agents that can solve new problems (IITP, Co-I, 2022 ~ 26, PI: Byoung-Tak Zhang)
- Center for Optimizing Hyperscale AI Models and Platforms (NRF, Co-I, 2023~, PI: Jaejin Lee)
- Scalable Causal Discovery (LG AI Research, PI, 2025 ~ 26)
- Advancing Credit Decision Making (AFINIT, PI, 2025 ~ 26)
- AI Platform for Predicting Drug Efficacy and Side Effects from Integrated Medical and Multi-omics Data (MFDS, Co-I, 2026 ~ 30)

### Past projects

- Semantic Search for Korean Medical and Legal Documents (SNU, co-PI, 2022~23, PI: Hyopil Shin)
- Association and Causality in Metabolomic data (MFDS, co-PI, 2022)
- Metabolomic Big Data Analysis (MFDS, Co-I, 2023 ~ 25)
- Supply Chain based Financial Keyword Analysis (NH Investment, 2021)
- Causal Discovery for Time Series (LG AI Research, PI, 2023.04~24.04)
- An algorithmic aspect of proxy-based causal inference (SNU, PI, 2021~24)
- Deep Generative Models for Causal Reasoning (LG AI Research, PI, 2024.05~25.05)
- Human-centric Embodied AI Agents with Autonomous Decision-Making (IITP, Co-I, 2025)

</details>
