# Apoena | RAG Engine & Context API

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## 1. Executive Summary
Apoena is a high-performance Retrieval-Augmented Generation (RAG) engine designed for high-fidelity context synthesis. It operates as an API-first service that processes, indexes, and retrieves semantic information from heterogenous data sources.

## 2. Technical Philosophy
The core objective is to minimize RAG latency and maximize retrieval precision. Apoena implements advanced chunking strategies and re-ranking pipelines to ensure that agents (like **Irú**) receive only the most relevant context, optimizing token consumption and execution costs.



## 3. Architecture & Data Flow
1. **Ingestion Layer:** Asynchronous document processing and sanitization.
2. **Embedding Engine:** Local or Cloud-based vectorization (OpenAI/HuggingFace).
3. **Vector Store:** **PostgreSQL + pgvector** for enterprise-grade persistence and relational filtering.
4. **Context API:** FastAPI endpoints providing streaming responses (Server-Sent Events).

## 4. Tech Stack
- **Engine:** Python 3.11+ (FastAPI).
- **Storage:** PostgreSQL (pgvector).
- **Infra:** Docker & Docker Compose.
- **Frontend:** Angular.

## 5. API Reference Summary
- `POST /v1/ingest`: Submit documents for vectorization.
- `POST /v1/search`: Execute semantic search with re-ranking.
- `GET /v1/context`: Synthesize final answer based on retrieved chunks.

---
