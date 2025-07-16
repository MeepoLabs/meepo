# Week 01 (Aug 4 – Aug 10 2025): Project Kick-off & RAG Foundation

## Overview
Kick-off the v0 initiative, choose core Retrieval-Augmented Generation (RAG) components, and scaffold both backend and frontend codebases.

## Tasks
### Research / Prototype
- [ ] Compare vector stores **Chroma**, **Supabase pgvector**, and **Qdrant**; document trade-offs and costs
- [ ] Spike data loaders with **LangChain** _and_ **LlamaIndex** for:
  - [ ] YouTube transcript ingestion
  - [ ] Generic web-page scraping
- [ ] Summarise findings in `docs/decision_records/0001-vector-store.md`

### Backend
- [ ] Bootstrap `backend/` FastAPI project
  - [ ] Initialise Poetry, enable Ruff & MyPy
  - [ ] Add Supabase JWT auth dependency (PoC)
  - [ ] Create `/healthz` endpoint
- [ ] Set up GitHub Actions for lint + tests

### Frontend
- [ ] Initialise SvelteKit project with TypeScript, Tailwind, shadcn-svelte
- [ ] Add basic layout & landing page placeholder

### Dev Ops
- [ ] Configure `.devcontainer.json` for VS Code / Codespaces
- [ ] Add pre-commit hooks (ruff, mypy, prettier)

## Deliverables
- Decision doc on vector DB + loader framework
- Running FastAPI skeleton
- SvelteKit skeleton
- CI pipeline passing on `main`

## Next Steps
Move to Week 02: implement ingestion endpoints and background worker.
