# Week 04 (Aug 25 – Aug 31 2025): Retrieval Pipeline & Evaluation

## Overview
Implement retrieval pipeline (similarity search + optional re‐ranking) and build a small evaluation harness to measure answer quality and latency. Build on the data processing foundation from Week 3.

## Tasks
### Research / Prototype
- [ ] Explore re-rankers (Cohere Rerank, OpenAI reordering) and decide if needed
- [ ] Design evaluation rubric (precision@k, latency, cost)

### Retrieval Backend
- [ ] `/query` endpoint accepting `{question}` and returning top-k docs
- [ ] Integrate retrieval with chosen vector DB API
- [ ] Optional: add re-rank stage toggle
- [ ] Cache results per user for 1 h (Redis)
- [ ] Add similarity search with configurable k parameter
- [ ] Implement metadata filtering for retrieval

### Evaluation Harness
- [ ] Create `scripts/evaluate.py` that runs predefined Q&A set
- [ ] Output metrics to CSV + markdown summary
- [ ] Add benchmarking for different embedding models
- [ ] Create evaluation dataset with ground truth Q&A pairs
- [ ] Implement precision@k, recall@k, and latency metrics

### Frontend
- [ ] Simple search box that displays retrieved chunks with highlight
- [ ] Latency + cost stats overlay
- [ ] "Add Source" form (URL + type) with progress indicator
- [ ] Table view of ingested sources with processing status

### Testing & Quality
- [ ] Integration tests for retrieval endpoints
- [ ] Performance tests for vector search
- [ ] Edge case testing (empty queries, malformed input)
- [ ] User experience testing for search interface

### Dev Ops
- [ ] Add GitHub Action to run evaluation on pull request label `eval`
- [ ] Update CI to run retrieval tests
- [ ] Add performance regression detection

## Deliverables
- Retrieval API with configurable k & rerank
- Evaluation script with baseline numbers
- Frontend search demo with source management
- Performance benchmarks and test coverage

## Next Steps
Buffer Week 05 for Phase 1 stabilization, catch-up, and integration testing.

## Notes
**Moved from original Week 3:**
- Retrieval pipeline implementation
- Evaluation harness and metrics
- Frontend search interface

This completes Phase 1 (Foundation & RAG) with a working end-to-end data ingestion and retrieval system.
