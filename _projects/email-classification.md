---
layout: page
title: Email Classification (Business vs. Personal)
description: Research on effective methods for classifying emails into business and personal categories using traditional and neural models.
img: https://images.unsplash.com/photo-1557075877-bf592ed513a7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1171&q=80
permalink: /projects/email-classification/
redirect: https://www.linkedin.com/in/milena-sosic/
importance: 8
category: research
back_url: /projects/
related_publications: vsovsic2022effective
---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/email-classification.jpg"
      title="Email classification concept"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>


## Overview

This project investigates practical and effective **email classification** methods for distinguishing between **business and personal emails** — a useful task for email management, automatic filtering, and conversational analysis.

The work combines **traditional machine learning**, **deep learning**, and **feature engineering** to explore how content, context, and auxiliary signals contribute to classification quality. 

---

## Problem Statement

Emails are one of the most widely used forms of communication. Despite advances in digital messaging, email remains dominant in both personal and professional contexts. Automatically classifying emails into categories such as *Business* and *Personal* can improve productivity and support downstream tasks such as prioritization, routing, and user profiling. :contentReference[oaicite:3]{index=3}

---

## Approach

The classification pipeline incorporates:

**Text representation:**
- Bag-of-Words (BoW) and **Tf-Idf** vectors on word and character n-grams  
- Contextual **BERT embeddings** for semantic features  

**Algorithms evaluation:**
- Traditional classifiers such as **SGD-optimized SVM** and **Extremely Randomized Trees**  
- Neural architectures like **BiLSTM and Attention-based BiLSTM** 

**Feature enrichment:**
Additional lexical, conversational, expressional, emotional, and moral features are extracted from content using custom lexicons and NLP techniques to enhance classification generalization. 

Variants of email content representation include:
- individual emails,
- emails with domain information,
- Arcs of conversational threads (branches). 

---

## Data & Evaluation

The experiments are performed on annotated versions of the **Enron email corpus**, a widely used benchmark for email research. Two distributions (*Enron Columbia* and *Enron Berkeley*) are used, with manual labels mapped into the *Business* or *Personal* classes. 

Evaluation uses standard classification measures (accuracy, precision, recall, F1), and the best configurations achieve **state-of-the-art results** on this task. 

---

## Key Contributions

- Comprehensive comparison of traditional and neural models on email classification  
- Exploration of multiple input representations (content, conversational context, domains)  
- Feature engineering including behavioral, emotional, and lexical signals  
- Openly available codebase for reproducibility and further research 

