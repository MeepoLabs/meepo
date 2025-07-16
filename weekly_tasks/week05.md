# Week 05 (Sep 1 – Sep 7 2025): Agent Scaffold

## Overview
Begin Phase 2 by creating the core agent abstraction, wiring it to the RAG backend, and exposing initial invocation endpoints.

## Tasks
### Research / Prototype
- [ ] Evaluate **LangChain Runnable** vs bespoke tool-executor; document pros/cons
- [ ] Define agent schema (name, system prompt, tools, memory config)

### Backend
- [ ] Implement `agents` CRUD endpoints (FastAPI `APIRouter`)
- [ ] Implement base `Tool` dataclass & registration decorator
- [ ] Wrap MCP utilities (`search`, `http`, etc.) as Tools
- [ ] Add `POST /agents/{id}/invoke` for single-turn chat

### Frontend
- [ ] "Create Agent" form (name, system prompt, tool multiselect)
- [ ] Agent list & delete actions

### Testing
- [ ] Unit tests for Tool registration & agent invocations (mock LLM)
- [ ] Contract tests for API schema with `pytest-asyncio`

## Deliverables
- Agent data model & API
- Minimal set of MCP tool wrappers
- UI to create & invoke agents

## Next Steps
Week 06 will integrate multi-provider LLMs and retrieval tool.
