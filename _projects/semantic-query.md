---
layout: page
title: Semantic Query Parsing
description: Semantic query interpretation for LLM-based retrieval and document search systems.
img: assets/img/query.png
importance: 3
category: work
back_url: /projects/
redirect: https://www.linkedin.com/in/milena-sosic/

---

## Overview

This project implements a **semantic query parsing pipeline** to convert raw user queries into **structured representations** for downstream tasks such as **Agentic RAG** ([see project](/projects/agentic-rag)).

---

## Implementation Details

- **Linguistic Preprocessing:** tokenization, normalization, part-of-speech tagging  
- **Intent Modeling:** transformer-based multi-intent classification, hierarchical labels  
- **Entity Extraction:** NER, domain-specific linking, slot filling  
- **Semantic Representation:** JSON, logical forms, graph structures  
- **Synthetic Query Generation:** LLM-guided paraphrasing, slot-preserving data augmentation  
- **Similarity & Retrieval:** Bi-encoder embeddings for retrieval, cross-encoder re-ranking  

---

## Integration with Agentic RAG

- Parsed semantic queries are fed into the **Planner Agent** for task decomposition  
- Enables **structured retrieval, grounded reasoning, and multi-step planning**  
- Works alongside **Prompt Engineering & Evaluation** for instruction optimization and observability

---

## Use Cases

- Knowledge-intensive search engines  
- Conversational agents with precise intent understanding  
- Recommendation systems  
- Analytics for query behavior and clustering