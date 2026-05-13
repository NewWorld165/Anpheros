# Anpheros
GDPR-compliant medical AI platform with RAG pipeline, semantic search, and LLM integration. Built with FastAPI, Flutter, PostgreSQL/pgvector, deployed on GCP.

# Anpheros — Medical AI Platform

> GDPR-compliant AI assistant for patients and clinicians.  
> Live at [anpheros.com](https://anpheros.com)

## What it does

Anpheros helps patients track their health and get AI-assisted insights from their own medical data — symptoms, documents, vitals, medications — while keeping all data private and compliant with GDPR Article 9.

## Architecture

```
Flutter (Web / iOS / Android)
        ↓
FastAPI Backend — Cloud Run (GCP)
        ↓
PostgreSQL + pgvector (Cloud SQL)
        ↓
RAG Pipeline → Claude / OpenAI / Ollama
```

## Key Technical Features

- **RAG pipeline built from scratch** — async vector embeddings, HNSW-indexed semantic search over patient health data
- **OCR document ingestion** — medical documents parsed, chunked, embedded, and searchable
- **Multi-LLM support** — Claude (Anthropic), OpenAI GPT-4, and local Ollama models
- **GDPR Article 9 compliant** — per-user data isolation, soft-delete, PII anonymisation before any AI call
- **Full CI/CD on GCP** — Cloud Build, Cloud Run, Alembic migrations, Nginx, Cloudflare

## Stack

| Layer | Technology |
|---|---|
| Frontend | Flutter (Dart) — Web, iOS, Android |
| Backend | FastAPI, Python, SQLAlchemy, Alembic |
| Database | PostgreSQL + pgvector (Cloud SQL) |
| AI/LLM | Claude API, OpenAI API, Ollama |
| Infrastructure | GCP Cloud Run, Cloud Build, Docker |
| Auth | Keycloak |

## Research

Actively exploring local LLM fine-tuning on Apple MLX (Mac Studio M4 Max) for Romanian-language medical AI with on-device inference — reducing cloud dependency and improving privacy.

## Status

Currently in **beta**. Built and maintained by [Kereky Adrian](https://anpheros.com) in collaboration with a medical advisor (MD).
```
