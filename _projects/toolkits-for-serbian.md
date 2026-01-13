---
layout: page
title: Toolkits for Serbian Language
description: NLP tools and linguistic resources developed or adapted for Serbian, covering preprocessing, annotation, and analysis.
img: https://images.unsplash.com/photo-1457369804613-52c61a468e7d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80
redirect: https://www.linkedin.com/in/milena-sosic/
importance: 7
category: research
related_publications: vsovsicsrpol
back_url: /projects/
---

Development of **NLP toolkits and linguistic resources for Serbian**, supporting preprocessing, morphology-aware analysis, annotation, and corpus exploration.

---

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/srpski.jpg"
      title="Text and language data"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/srpski1.jpg"
      title="Data processing pipelines"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/srpski2.jpg"
      title="Engineering tools"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>

---

## Overview

This project groups together **toolkits, scripts, and linguistic resources** developed or adapted for **Serbian language processing**.
The focus is on **practical NLP support** for a morphologically rich, under-resourced language, enabling downstream tasks such as classification, extraction, and corpus analysis.

Rather than a single system, this is a **collection of interoperable tools** used across multiple projects.

---

## Preprocessing & normalization

Core preprocessing components include:

- **Text normalization** (Unicode, diacritics, casing)
- **Tokenization** adapted to Serbian specifics
- Handling of:
  - Latin and Cyrillic scripts
  - informal and social-media text
  - punctuation, emojis, and non-standard word forms

These steps were designed to be reusable and configurable depending on the task.

---

## Morphology & lexical resources

Work with Serbian lexical and morphological resources included:

- **lemmatization and morphological features**
- integration of **lexicons** (emotion, sentiment, domain-specific)
- use of **WordNet-style resources** for semantic alignment and enrichment

Special attention was paid to:
- inflectional variation,
- negations, derivations and variations,
- ambiguity introduced by rich morphology.

---

## Annotation & extraction tools

Toolkits also covered **annotation and information extraction**, such as:

- scripts for **manual and semi-automatic annotation** inlcudin **outputs validation**
- **named entity extraction** (general and domain-specific)
- extraction of linguistic cues (keywords, patterns, markers)

These tools were used to bootstrap datasets and to support iterative annotation workflows.

---

## Corpus analysis & utilities

Additional utilities include:

- frequency and co-occurrence analysis,
- n-gram and subword statistics,
- corpus-level summaries and diagnostics,
- export to formats suitable for ML pipelines.

The emphasis was on **transparent, inspectable outputs** rather than black-box processing.

---

## Why this matters

For Serbian, high-quality NLP often depends on **custom tooling** rather than off-the-shelf solutions.
This collection of toolkits enabled:

- faster dataset creation,
- consistent preprocessing across projects,
- reproducible experiments,
- and easier adaptation of models developed for high-resource languages.

---

## SRPOL: A Lexicon-Based Framework for Sentiment Strength in Serbian

**SRPOL** is a **lexicon-based sentiment analysis framework for Serbian**, designed to estimate both **sentiment polarity and sentiment strength** in texts from the political and public discourse domain.

The framework is centered around a **manually curated and corpus-expanded sentiment lexicon** for Serbian, comprising approximately **15,000 lexical entries**, enriched with polarity values and sentiment intensity information. In addition to core sentiment-bearing words, SRPOL incorporates **contextual sentiment triggers** that influence sentiment strength at the sentence level.

The resource was developed to address the lack of high-quality sentiment lexicons for Serbian and to support **linguistically informed sentiment analysis** in a morphologically rich, under-resourced language.

SRPOL has been evaluated on Serbian textual data from multiple domains and demonstrates competitive performance in sentiment strength detection, making it suitable both as a standalone lexicon-based solution and as a supporting component in hybrid or supervised NLP pipelines.

---




