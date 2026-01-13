---
layout: page
title: Other NLP Projects
description: A collection of applied NLP projects including text classification, entity extraction, and syllable identification.
img: https://images.unsplash.com/photo-1620712943543-bcc4688e7485?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=765&q=80
# redirect: https://www.linkedin.com/in/milena-sosic/
importance: 6
category: work
back_url: /projects/
redirect: https://www.linkedin.com/in/milena-sosic/
---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/topic-modeling.jpg"
      title="Genome / sequencing concept"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>

Applied NLP projects covering **text classification**, **entity extraction**, and **subword-level analysis**, with emphasis on linguistic structure, evaluation, and practical modeling trade-offs.
---

## Overview

This page summarizes a set of **smaller-scale NLP projects and experiments** developed across different contexts (academic, exploratory, and applied work).
While diverse in scope, all projects focus on **linguistic structure, representation, and supervised or weakly supervised learning**.

They complement larger, standalone projects by demonstrating **breadth of NLP techniques** and hands-on experimentation.

---

## Text classification

Work on text classification covered multiple problem settings:

- **Binary and multi-class classification**  
  (e.g., topic detection, sentiment polarity, domain classification)
- **Multi-label classification**  
  where documents may belong to several categories simultaneously
- Feature-based and neural approaches:
  - bag-of-words / TF–IDF
  - n-grams
  - neural embeddings (CNN/RNN-based encoders, later transformer-based)

Focus areas included:
- feature engineering vs. representation learning,
- class imbalance handling,
- model evaluation beyond accuracy (precision/recall/F1).

---

## Named Entity Extraction

Several projects explored **entity extraction and sequence labeling**, including:

- rule-based and statistical approaches for **named entity recognition (NER)**,
- extraction of **domain-specific entities** (non-standard entity sets),
- token-level labeling using BIO-style schemes.

Key aspects:
- tokenization and normalization challenges,
- ambiguity and boundary detection,
- error analysis at the span level rather than token level.

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/namedentity.png"
      title="Genome / sequencing concept"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>

---

## Syllable identification and subword analysis

Another line of work focused on **subword-level linguistic structure**, including:

- **syllable identification** in words,
- analysis of phonotactic and orthographic patterns,
- rule-based and data-driven heuristics for syllabification.

This work highlighted:
- the importance of linguistic constraints,
- limitations of purely statistical approaches on small datasets,
- usefulness of hybrid rule + ML solutions.

---

## Common themes across projects

Across these NLP projects, recurring themes include:

- careful **problem formulation**,
- explicit handling of **linguistic structure** (tokens, subwords, entities),
- strong emphasis on **evaluation and error analysis**,
- preference for **interpretable baselines** before complex models.

---

