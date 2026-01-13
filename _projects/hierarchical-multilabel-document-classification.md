---
layout: page
title: Hierarchical Multilabel Document Classification
description: Hierarchical multi-label document categorization using a label taxonomy (tree/DAG) and neural + classical baselines.
img: https://images.unsplash.com/photo-1504711331083-9c895941bf81?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80
importance: 4
category: work
back_url: /projects/
redirect: https://www.linkedin.com/in/milena-sosic/

---

## Overview

This project focuses on **hierarchical multi-label document classification (HMLC)** — assigning **multiple labels** to each document, where labels are organized in a **hierarchy** (e.g., *Category → Subcategory → Group → Subgroup*). Unlike “flat” multi-label classification, HMLC explicitly models **parent–child relations** between categories.

- **Task:** multi-label document classification with a predefined taxonomy  
- **Output:** one or more **paths** in the hierarchy (multiple labels per document)

---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/document-classification.jpg"
      title="Documents classification concept"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>

---

## How it works

A hierarchical label structure has been emplyed to classify documents into their appropriate categories with the goal to explore:
- how hierarchical constraints affect prediction quality,
- how multi-level labels can be represented (per-level indices vs. global label ids),
- and how different models behave when labels are not independent.

## Data & label structure (example)

Documents are represented with text fields (e.g., title/abstract) and assigned (hierarchical) labels.  
A typical record contains tokenized text plus labels at each level and a combined list of label ids:

- `title`, `abstract`: tokenized text
- `section / subsection / group / subgroup`: indices at each hierarchy level
- `labels`: encoded into label ids (using per-level offsets)

<!-- > This format makes it easy to train with per-level supervision and/or a unified multi-label head. -->

## Modeling

Approaches explored/used (depending on experiment scope):

- **Hierarchy-aware neural model** (e.g., attention + recurrent encoder with hierarchical output heads)
- **Multi-label baselines** (flat vs. hierarchical)
- **Evaluation with hierarchy in mind** (per-level accuracy/F1 and overall multi-label metrics)

## Why hierarchy helps

A hierarchy provides:
- **regularization** (predictions are constrained by parent labels),
- **better interpretability** (you can explain predictions as paths),
- and a natural way to handle **fine-grained label spaces**.

---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/mermaid-hierarchy1.png"
      title="Category hierarchy concept"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>
---

