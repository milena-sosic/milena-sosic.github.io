---
layout: page
title: Documents Search & Answer
description: Improving search quality with ranking, relevance signals, and evaluation (LTR + neural re-ranking).
img: assets/img/search.jpg
# img: https://images.unsplash.com/photo-1477013743164-ffc3a5e556da?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1170&q=80
redirect: https://www.linkedin.com/in/milena-sosic/
importance: 5
category: work
back_url: /projects/
---

## Overview

This project focuses on **search relevance**: given a user query, rank candidate documents/results so that the most useful items appear at the top.
The work combines **information retrieval (IR)** principles with **learning-to-rank** and **neural re-ranking** to improve end-to-end retrieval quality.

Typical applications: enterprise search, e-commerce search, knowledge-base search, and semantic search over large text collections.

## Problem framing

We model search as a ranking task:

- **Input:** query + a set of candidate documents (title/body/metadata)
- **Output:** a ranked list, optimized for user satisfaction and business goals
- **Key challenges:** ambiguous queries, long-tail, synonyms, multilingual/typos, sparse clicks, position bias, cold-start

## Approach (high level)

A practical relevance stack usually looks like this:

1. **Retrieval (candidate generation)**  
   - lexical retrieval (e.g., BM25 / TF-IDF) and/or dense retrieval (embeddings)
2. **Re-ranking (quality boost on top candidates)**  
   - gradient-boosted rankers (LambdaMART-style) and/or neural cross-encoders
3. **Calibration & business rules (optional)**  
   - diversity, freshness, de-duplication, policy constraints

## Signals & features

Examples of relevance signals that can be incorporated:

- **Text relevance:** query–title/body matches, term proximity, field boosts
- **Semantic relevance:** dense embeddings similarity, synonym/intent matching
- **Behavioral signals:** clicks, dwell time, add-to-cart / conversions (with debiasing)
- **Document quality:** authority, recency, popularity, spam indicators
- **Query features:** length, intent type, detected entities, language

## Evaluation

Relevance work lives or dies by measurement. Common evaluation setup:

- **Offline metrics:** nDCG@k, MRR@k, MAP, Recall@k
- **Human judgments:** graded relevance labels (0–3) for query–doc pairs
- **Online validation (if available):** A/B tests, interleaving, CTR + downstream KPI

## Deliverables / outputs

- A reproducible **evaluation pipeline** (datasets, splits, metrics)
- Baselines (lexical retrieval) + improved ranker (LTR / neural reranker)
- Error analysis: query classes, failure modes, feature importance, model drift checks

---

## Visuals

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80"
      title="Search and ranking (concept)"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80"
      title="Evaluation and analytics"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="https://images.unsplash.com/photo-1558494949-ef010cbdcc31?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80"
      title="Systems and infrastructure"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>
<div class="caption">
  Conceptual visuals (Unsplash): search/ranking, evaluation analytics, and scalable systems.
</div>

## One-liner (for CV)

**Search relevance optimization**: candidate retrieval + learning-to-rank / neural re-ranking, with rigorous offline evaluation (nDCG/MRR) and relevance-driven error analysis.