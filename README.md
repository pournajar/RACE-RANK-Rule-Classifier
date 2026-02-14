# RACE-RANK  
## A Hybrid Rule-Based Classifier Using PageRank Algorithm

---

## 📖 Overview

**RACE-RANK** is a hybrid rule-based classification framework that enhances the Rule Aggregation ClassifiER (RACER) by introducing a graph-based rule ordering mechanism using the PageRank algorithm.

Rule-based classifiers are widely used in domains such as healthcare, finance, and cybersecurity due to their interpretability and strong predictive performance. Although RACER demonstrates high effectiveness, it faces two main challenges:

1. Rule ordering can significantly influence classification accuracy.
2. Excessive rule merging may lead to over-generalization and reduced performance.

RACE-RANK addresses these issues by:

- Applying a PageRank-based graph model to rank and organize rules.
- Introducing a controlled stopping strategy that halts rule merging after the first iteration.

The proposed method improves classification performance while preserving interpretability.

## 🧠 Methodology

RACE-RANK consists of three main components:

### 1️⃣ Initial Rule Generation
Rules are generated using the original RACER framework.

### 2️⃣ Graph-Based Rule Ranking
- Each rule is represented as a node in a graph.
- Relationships between rules define edges.
- Rule importance is computed using:
  - **PageRank** (primary method)
  - Betweenness Centrality (for comparison)
  - Eigenvector Centrality (for comparison)

The ranked rules are then used in the classification process.

### 3️⃣ Controlled Rule Merging

Unlike RACER, which may continue merging rules until convergence, RACE-RANK:

- Stops merging after the first iteration.
- Prevents excessive generalization.
- Maintains discriminative rule quality.



## 📊 Experimental Evaluation

RACE-RANK was evaluated on:

- **29 benchmark datasets**
  - UCI Machine Learning Repository
  - OpenML

### Comparisons

- RACER
- 14 additional machine learning classifiers
- Alternative ranking strategies:
  - Betweenness Centrality
  - Eigenvector Centrality

### Evaluation Metrics

- Accuracy
- F1-Score

Experimental results demonstrate consistent improvements over RACER in both accuracy and F1-score.

# Available Options

```
--ranking_method    pagerank | betweenness | eigenvector
--merge_strategy    controlled | full
--metric            accuracy | f1
```

# 🚀 Usage

Run the main experiment:

```
python main.py --dataset DATASET_NAME
 ```

Example:

```
python main.py --dataset adult
```

# 📌 Citation
If you use this work in your research, please cite:

```
@article{yourcitation2025,
  title={RACE-RANK: A Hybrid Rule-Based Classifier Using PageRank Algorithm},
  author={Alireza Basiri, Nasrin Pournajar},
  journal={Applied Soft Computing},
  year={2025}
}
```

Read the full paper on Applied Soft Computing Journal:
[RACE-RANK: A hybrid rule-based classifier using PageRank algorithm](https://www.sciencedirect.com/science/article/abs/pii/S1568494625015261)

## 🙏 Acknowledgment

This work is based on the original **ROPAC: rule optimized aggregation classifier** algorithm.

Original paper:
Mokhtari, Melvin, and Alireza Basiri, *ROPAC: rule optimized aggregation classifier*, Expert Systems with Applications , 2024.  
[ROPAC: rule optimized aggregation classifier](https://www.researchgate.net/profile/Melvin-Mokhtari/publication/379633484_ROPAC_Rule_OPtimized_Aggregation_Classifier/links/661c134466ba7e2359d96b6d/ROPAC-Rule-OPtimized-Aggregation-Classifier.pd)


# 🤝 Contributing

Contributions, suggestions, and bug reports are welcome.
Please open an issue or submit a pull request.

