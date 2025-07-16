# Week 03 (Aug 18 – Aug 24 2025): Data Loaders & Background Workers

## Overview
Implement background processing, vector embeddings, and advanced data loaders. Build on the solid database foundation from Week 2.

## Tasks
### Vector Database Setup
- [ ] Finalize choice of vector DB based on Week 01 findings (Chroma/pgvector/Qdrant)
- [ ] Set up vector database connection and configuration
- [ ] Implement vector storage operations (insert, search, delete)
- [ ] Benchmark embedding models (OpenAI vs Instructor vs Mistral) on sample set

### Background Processing
- [ ] Choose between Celery (Redis) and lightweight RQ; implement chosen solution
- [ ] Set up Redis for queue and caching
- [ ] Create background task for content processing:
  - [ ] Download/scrape content
  - [ ] Generate embeddings using chosen model
  - [ ] Store vectors with metadata
  - [ ] Update source status
- [ ] Add retry logic and error handling for failed tasks
- [ ] Implement task progress tracking

### Advanced Data Loaders
- [ ] Implement PDF loader using Unstructured.io or LangChain
- [ ] Implement Docx loader
- [ ] Implement GitHub repository loader (README + docs)
- [ ] Add content-type detection and routing
- [ ] Implement incremental updates using content hashes

### Backend Enhancements
- [ ] Update `/sources` POST to trigger background processing
- [ ] Add `/sources/{id}/chunks` endpoint to view processed content
- [ ] Implement chunking strategies (sentence-window, semantic chunks)
- [ ] Add metadata extraction for different content types

### Development Environment
- [ ] Docker-compose for local dev with worker + Redis + vector DB
- [ ] Add worker monitoring and logging
- [ ] Create Makefile targets (`make up`, `make test`, `make worker`)

### Testing
- [ ] Integration tests with mocked embedding APIs
- [ ] End-to-end tests for background processing pipeline
- [ ] Load tests with multiple concurrent ingestion tasks

## Deliverables
- Complete background processing pipeline
- Vector embedding and storage working
- Advanced loaders (PDF, GitHub, Docx) functional
- Docker development environment

## Next Steps
Week 04 will focus on retrieval pipeline and evaluation harness.

## Notes
**Added from original Week 2:**
- Background workers and queue setup
- Vector embeddings and database setup
- PDF/GitHub/Docx loaders
- Docker-compose development environment

This week builds the core data processing engine on the database foundation from Week 2.
