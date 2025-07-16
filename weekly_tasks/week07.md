# Week 07 (Sep 15 – Sep 21 2025): LLM Integration & Tool System

## Overview
Connect agents to multiple LLM providers through LiteLLM, add retrieval tool, and expose temperature/system-prompt controls. Build on the authentication and agent foundations from Week 6.

## Tasks
### Research / Prototype
- [ ] Evaluate cost/perf across OpenAI, Claude, Gemini using LiteLLM bench script
- [ ] Compare prompt-tuning vs LoRA fine-tuning on small set
- [ ] Compare OpenAI moderation vs self-hosted **GuardrailAI**

### LLM Integration
- [ ] Integrate **LiteLLM** client; support model routing via env
- [ ] Add agent runtime config: `temperature`, `top_p`, `model`
- [ ] Implement provider failover and retry logic
- [ ] Add cost tracking per LLM provider

### Tool System
- [ ] Implement `RetrievalTool` that calls `/query` internally
- [ ] Wrap MCP utilities (`search`, `http`, etc.) as Tools
- [ ] Add tool parameter validation and error handling
- [ ] Create tool discovery and registration system

### Basic Guardrails
- [ ] Implement content-filter middleware (moderation API)
- [ ] Add rate-limit decorator (per-IP & per-user quotas)
- [ ] Support prompt template versions per agent
- [ ] Store execution logs in Supabase `logs` table

### Frontend
- [ ] Update agent form with provider/model dropdown & sliders
- [ ] UI for editing prompt templates (markdown editor)
- [ ] Display moderation errors to user politely
- [ ] Tool selection interface for agents

### Testing
- [ ] Latency & cost benchmark script `scripts/llm_bench.py`
- [ ] Unit tests for RetrievalTool and tool system
- [ ] Red-team prompts to verify guardrails
- [ ] Unit tests for rate-limit logic

## Deliverables
- Multi-provider LLM support
- Retrieval tool wired into agent executions
- Basic guardrails (moderation + rate limits)
- Prompt template editor

## Next Steps
Week 08 will add streaming support and secret management.

## Notes
**Added from original Week 6:**
- Multi-provider LLM integration with LiteLLM
- Tool system implementation
- Retrieval tool integration

**Added from original Week 7:**
- Basic guardrails and content filtering
- Prompt template system

This combines LLM capabilities with basic safety measures.
