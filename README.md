Source-Grounded RAG – Learning Project

Overview

This repository documents a learning project where I built a source-grounded AI system using Retrieval-Augmented Generation (RAG). The goal was not to build a production-ready application, but to deeply understand how AI systems can be constrained to answer only from trusted source material and refuse when the source does not support an answer.

The project was built as a hands-on exploration while working in the product domain, without prior full-stack or deep backend engineering experience.

⸻

Why this project

The idea came from observing how a human expert develops knowledge by reading, cross-referencing, and reasoning strictly from authoritative texts. I wanted to test whether an AI system could be designed to follow the same discipline.

Astrology is used here only as a test domain because it:
	•	Has well-defined classical texts
	•	Contains multiple systems that must not be mixed
	•	Is highly prone to hallucination if constraints are weak

This makes it a strong stress test for trust, boundaries, and retrieval accuracy.

⸻

What this project demonstrates
	•	Retrieval-Augmented Generation (RAG) architecture
	•	Source-bound answer generation
	•	Explicit refusal when information is not present in sources
	•	Separation of knowledge ingestion from query logic
	•	Product-first experimentation with AI systems

⸻

What this project is NOT
	•	Not a predictive or advisory system
	•	Not a finished or monetized product
	•	Not a replacement for domain experts
	•	Not a demonstration of astrology accuracy

The focus is AI system design, not domain claims.

⸻

Architecture (High Level)
	1.	Source documents are placed in data/books
	2.	Documents are ingested and chunked
	3.	Text chunks are converted into embeddings
	4.	Embeddings are stored locally as a vector store
	5.	User queries retrieve only the most relevant chunks
	6.	The AI model explains only what the retrieved sources contain

⸻

Tech Stack
	•	Python
	•	FastAPI
	•	LlamaIndex
	•	OpenAI API
	•	FAISS / local vector storage

⸻

Project Structure

ai-astrology-rag/
├── api/            # Query and chat API
├── services/       # Ingestion logic
├── data/
│   ├── books/      # Source documents (not committed)
│   └── vector_store/ # Generated embeddings (ignored)
├── main.py         # App entry point
├── requirements.txt
└── README.md


⸻

How to run locally
	1.	Clone the repository
	2.	Create a virtual environment
	3.	Install dependencies
	4.	Add your own documents to data/books
	5.	Run ingestion
	6.	Start the FastAPI server

(API keys and generated data are intentionally excluded from the repo.)

⸻

Key learning

Modern AI tooling significantly lowers the barrier to building first versions of products. However, it also shifts the challenge toward:
	•	Clear problem framing
	•	Source selection and discipline
	•	Boundary design (what the system must not do)
	•	Trust and refusal behavior

This project was a strong reminder that thinking and system design matter more than code volume.

⸻

Status

Early-stage learning project. Still evolving.