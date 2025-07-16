# Meepo Platform – MVP Requirements (v0.1.0)

_Last updated: 15 Jul 2025_

## 1. Purpose
Deliver a minimal yet end-to-end “vertical slice” of the Meepo Platform that allows a user to:
1. **Load data** from common public sources (YouTube videos, generic web pages).
2. **Ask questions** over that data using an agent powered by state-of-the-art LLMs.
3. **Automate output** by pushing the agent’s response to external destinations (e.g., Twitter threads, WordPress posts, generic HTTP hooks).
4. **Interact** with the agent through a real-time chat UI that can be embedded in other sites.

## 2. Out-of-Scope for MVP
The following features are deferred to later releases:
- Visual drag-and-drop builder.
- Multi-framework adapters via **pymeepo**.
- Enterprise multi-tenant controls (RBAC, VPC peering, SOC-2, etc.).
- Advanced monitoring dashboards and marketplace component discovery.

## 3. Functional Requirements
### 3.1 Data Ingestion & RAG (Phase 1)
- R-001 User can submit a YouTube URL; system stores transcript and metadata.
- R-002 User can submit a generic web URL; system scrapes page text.
- R-003 Content is chunked and embedded; vectors are stored in the chosen Vector DB.
- R-004 Ingestion status can be queried via API and UI.

### 3.2 Retrieval & Evaluation (Phase 1)
- R-005 API `/query` returns top-_k_ relevant chunks for a given question.
- R-006 Optional re-ranking stage can be toggled via query parameter.
- R-007 Evaluation harness produces precision@_k_, latency, and cost metrics.

### 3.3 Agent Orchestration (Phase 2)
- R-008 Agents have a schema: `name`, `system_prompt`, `tools[]`, `model_cfg`.
- R-009 Built-in Tools: `RetrievalTool`, `SearchTool`, `HttpTool`.
- R-010 Agents can be invoked synchronously (`POST /agents/{id}/invoke`).
- R-011 Execution logs (prompt, response, cost, latency) are stored in DB.
- R-012 LiteLLM enables routing across OpenAI, Claude, Gemini providers.

### 3.4 Guardrails & Cost Optimisation (Phase 2)
- R-013 Content moderation filter blocks disallowed output.
- R-014 Rate limiting enforced per user and per IP.
- R-015 Cost tracker records tokens & $ per invocation; available via API.

### 3.5 Output Integrations (Phase 3)
- R-016 System can post a Twitter thread via OAuth 2.0.
- R-017 System can create a draft WordPress post via REST/XML-RPC.
- R-018 System can POST arbitrary JSON to a user-defined webhook URL.
- R-019 Execution status (success/failure) is viewable in UI and retriable.

### 3.6 Chat UI & Embeddable Widget (Phase 3)
- R-020 Real-time chat component streams agent responses with citations.
- R-021 Theme switch (light/dark) is available.
- R-022 Widget can be embedded via `<script>` tag on external sites.

### 3.7 Authentication & Security
- R-023 Users authenticate via Supabase JWT; tokens stored in http-only cookies.
- R-024 External integrations use OAuth 2.0 (PKCE) where applicable.
- R-025 Secrets are encrypted at rest; CI runs secret-scanning on every PR.

### 3.8 Observability
- R-026 Structured logs via `structlog`.
- R-027 Prometheus metrics exposed at `/metrics`.
- R-028 OpenTelemetry traces exported to Grafana Tempo.

### 3.9 Deployment & Dev Ops
- R-029 Backend containerised; deployed to **GCP Cloud Run** via Terraform.
- R-030 Frontend deployed to **Cloudflare Pages** with custom domain & SSL.
- R-031 CI (GitHub Actions) runs lint, tests, evaluation harness, and—not on forks—deploys to staging.

### 3.10 Additional Enhancements (cross-phase)
- R-032 System supports PDF/Docx and GitHub repository loaders.
- R-033 Ingestion pipeline performs incremental updates using content hashes.
- R-034 Users can securely store and manage API keys/secrets via a vault UI and API.
- R-035 Usage dashboard shows daily tokens, embeddings, output tasks, and cost.
- R-036 Official SDKs (Python & JS) and a CLI allow programmatic ingestion/query.
- R-037 Embeddable widget supports end-user authentication via developer-signed JWT or magic link flow.
- R-038 Platform can send agent outputs to Slack or Discord via webhook tasks.

## 4. Non-Functional Requirements
| Attribute | Target |
|-----------|--------|
| CI success rate | 100 % on `main` |
| Unit-test coverage | ≥ 80 % for backend, ≥ 70 % for frontend |
| p95 chat latency | ≤ 750 ms |
| Uptime | ≥ 99 % during beta |
| Cost tracking granularity | per invocation + per user per day |

## 5. Technology Stack
- **Backend** Python 3.10+, FastAPI, Pydantic v2, Poetry, LiteLLM, Supabase (Postgres + Storage), Vector DB (Chroma/pgvector/Qdrant), Redis (queue & cache).
- **Frontend** SvelteKit, TypeScript, Tailwind CSS, shadcn-svelte, Playwright tests.
- **Infrastructure** Cloud Run, Cloudflare Pages, Terraform, GitHub Actions.
- **Observability** structlog, Prometheus, Grafana Tempo, Grafana Cloud Dashboards.

## 6. Timeline & Milestones
| Phase | Weeks | Milestone |
|-------|-------|-----------|
| Phase 1 | 1 – 3 | Ingestion & RAG live on staging |
| Buffer A | 4 | Phase 1 stabilised |
| Phase 2 | 5 – 8 | Agent orchestration + guardrails complete |
| Buffer B | 9 | Phase 2 stable |
| Phase 3 | 10 – 12 | Output integrations + chat UI functional |
| Buffer C | 13 | Phase 3 stable |
| Phase 4 | 14 – 15 | Production deployment & beta release |
| Buffer D | 16 | Post-QA polish & v0.2 planning |

---

This document supersedes high-level sections of the full `requirements.md` for the purposes of the MVP cycle only. Future phases will reference the original comprehensive specification once v0.1.0 is shipped.
