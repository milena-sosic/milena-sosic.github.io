---
layout: page
title: Prompt Engineering & Evaluation
description: Systematic prompt optimization, observability, and evaluation for LLM-based RAG systems.
img: assets/img/prompt1.png
importance: 2
category: work
back_url: /projects/
redirect: https://www.linkedin.com/in/milena-sosic/
---

## Overview

This project establishes a **structured framework for prompt engineering** across multiple LLM tasks, including **Agentic RAG** ([see project](/projects/agentic-rag)).

It combines:
- **DSPy**: programmatic prompt optimization  
- **Langfuse**: observability, logging, and debugging  
- **ragas**: quantitative evaluation for RAG systems  

---

## Implementation Highlights

- **Prompt Templates:** Structured JSON/markdown outputs, instruction tuning  
- **Programmatic Tuning:** DSPy allows parameterized prompts with metric-guided optimization  
- **Monitoring:** Langfuse tracks prompt execution, token usage, latency, and errors  
- **Evaluation:** ragas evaluates faithfulness, evidence recall, and answer relevance  

---

## Techniques

- Ensemble prompts with voting / majority selection  
- Self-critique and automatic revision loops  
- Regression testing of prompts across LLM versions  
- Cross-model validation for reliability and robustness  

---

## Outcomes

- Improved answer accuracy and faithfulness  
- Reduced prompt brittleness  
- Faster experimentation cycles  
- Transparent, auditable behavior for production-ready LLM systems