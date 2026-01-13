---
layout: page
title: Agentic RAG for Documents Exploration
description: Agent-based Retrieval-Augmented Generation for complex document search using LangChain and LangGraph.
img: assets/img/rag.png
importance: 1
category: work
back_url: /projects/
redirect: https://www.linkedin.com/in/milena-sosic/
---

## Overview

This project implements **Agentic Retrieval-Augmented Generation (Agentic RAG)** for **document-centric QA and search**, integrating **LangChain** for agent orchestration and **LangGraph** for workflow visualization and reasoning tracking.

Unlike traditional RAG, this system uses **autonomous agents** that iteratively retrieve, reason, verify, and refine answers based on document context.

See also: [Semantic Query Parsing](/projects/semantic-query) for the query understanding component and [Prompt Engineering & Evaluation](/projects/prompt-engineering) for prompt optimization strategies.

---

## Implementation Details

- **Frameworks:** LangChain (agent orchestration), LangGraph (workflow graphing)
- **Retriever:** Dense embeddings (OpenAI / SentenceTransformers), BM25 sparse retrieval, hybrid ranking
- **Agents:**  
  - **Planner Agent:** decomposes queries into sub-tasks  
  - **Retriever Agent:** executes multi-strategy retrieval  
  - **Reasoning Agent:** applies chain-of-thought reasoning, step-wise synthesis  
  - **Verifier Agent:** validates facts, detects hallucinations
- **Indexing:** Chunked documents, hierarchical sections, overlapping windows
- **Evidence Attribution:** Each answer includes references to the original document chunks

---

## Workflow

1. User query → **Semantic Query Parser** ([see project](semantic-query))
2. Planner decomposes query → selects retrieval strategy
3. Retriever pulls relevant documents (dense + sparse)
4. Reasoning agent generates grounded answer
5. Verifier checks consistency and confidence
6. Agent iteratively refines until threshold confidence is reached

---

## Advanced Techniques

- Iterative RAG loops: retrieve → reason → retrieve  
- Self-reflection and hallucination detection  
- Tool-aware prompt management via [Prompt Engineering & Evaluation](/projects/prompt-engineering)  
- Automated answer abstention if evidence is insufficient

---

## Evaluation & Use Cases

- Enterprise knowledge search  
- Scientific and technical QA  
- Legal and regulatory compliance analysis  
- Human-in-the-loop verification and iterative improvement