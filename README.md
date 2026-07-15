<div align="center">

# 📚 Source-Grounded RAG

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![LlamaIndex](https://img.shields.io/badge/LlamaIndex-6d28d9?style=for-the-badge)
![FAISS](https://img.shields.io/badge/FAISS-0467DF?style=for-the-badge)
![Learning Project](https://img.shields.io/badge/Learning_Project-4c1d95?style=for-the-badge)

**A RAG system designed to answer *only* from trusted sources — and refuse when they don't support an answer.**

</div>

---

## Overview
A learning project building a **source-grounded AI system** using Retrieval-Augmented
Generation. The goal wasn't a production app — it was to deeply understand how an AI
can be **constrained to trusted material** and made to **refuse** when the source
doesn't back an answer. Built as a hands-on exploration from a **product background**,
without prior deep backend experience.

## Why this project
It came from watching how a human expert builds knowledge: reading, cross-referencing,
and reasoning strictly from authoritative texts. Could an AI follow the same discipline?

**Astrology is used only as a test domain** — because it has well-defined classical
texts, multiple systems that must not be mixed, and is highly prone to hallucination if
constraints are weak. That makes it a strong stress test for **trust, boundaries, and
retrieval accuracy**. (The focus is AI system design, not domain claims.)

## What it demonstrates
- Retrieval-Augmented Generation (RAG) architecture
- **Source-bound** answer generation + **explicit refusal** when info isn't present
- Separation of knowledge ingestion from query logic
- Product-first experimentation with AI systems

## Architecture
```
data/books ──► ingest + chunk ──► embeddings ──► local vector store (FAISS)
                                                        │
              user query ──► retrieve top chunks ──► model answers ONLY from them
```

## Tech stack
`Python` · `FastAPI` · `LlamaIndex` · `OpenAI API` · `FAISS / local vector store`

## Run locally
```bash
# clone → venv → install deps → add your docs to data/books → run ingestion → start FastAPI
```
*(API keys and generated data are intentionally excluded from the repo.)*

## Key learning
Modern AI tooling drastically lowers the barrier to a first version — but shifts the real
challenge to **problem framing, source discipline, boundary design, and refusal
behavior**. A strong reminder that **thinking and system design matter more than code
volume**.

<div align="center"><sub>Early-stage learning project by <b>Tanishq Jain</b> · still evolving</sub></div>
