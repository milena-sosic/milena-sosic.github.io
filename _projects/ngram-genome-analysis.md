---
layout: page
title: N-gram genome analysis
description: Alignment-free detection of genomic islands in bacterial genomes using n-gram language models, Markov chains, and C4.5 (2010).
img: https://images.unsplash.com/photo-1655993810480-c15dccf9b3a0?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=80
importance: 10
category: research
back_url: /projects/
redirect: https://www.linkedin.com/in/milena-sosic/
---

## Overview

This project explored **alignment-free identification of genomic islands** in bacterial genomes by modeling nucleotide sequences as a “language”.
The goal was to distinguish **genomic islands vs. the rest of the sequence** based on differences in **nucleotide composition and local n-gram patterns**.

- **Year:** 2010  
- **Status:** internal research (not published), no public repository  
- **Domain:** bacterial genomics, sequence segmentation / classification

---
<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.html
      path="assets/img/nucleotide.jpg"
      title="Genome / sequencing concept"
      class="img-fluid rounded z-depth-1"
    %}
  </div>
</div>

**Alignment-free genomic island detection** in bacterial genomes using **k-mer (n-gram) language models**, **Markov chains**, and **C4.5** for region classification (2010).
---

## Approach

We treated DNA as a sequence over the alphabet {A, C, G, T} and used:

- **n-gram language models** (k-mers) to capture local composition
- **Markov chain models** to estimate transition structure / likelihoods
- **C4.5 decision tree** for supervised classification of windows/regions

Typical workflow:

1. **Windowing/segmentation** of genome into fixed-length or sliding windows  
2. **Feature extraction** from each window  
   - n-gram frequency profiles (optionally normalized)
   - Markov-based scores (e.g., likelihood under background vs. island model)
3. **Classification** (C4.5) to label windows/regions as *island* vs. *non-island*  
4. **Post-processing** to merge consecutive windows into candidate islands

## Notes on signals (intuition)

Genomic islands often differ from the host genome due to horizontal transfer, so they may show:
- shifts in **k-mer distribution**
- changes in **transition probabilities** between nucleotides
- detectable boundaries when comparing local (island) statistics vs. genome-wide baseline




