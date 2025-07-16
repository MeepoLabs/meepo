# Week 02 (Aug 11 – Aug 17 2025): Database Design & Basic Ingestion

## Overview
Design core database schemas and implement basic ingestion capability. Focus on solid foundations before adding complexity.

## Tasks
### Database Design
- [ ] Design core database schemas:
  - [ ] `sources` table (id, url, type, status, metadata, created_at, updated_at)
  - [ ] `chunks` table (id, source_id, content, embedding_id, position, metadata)
  - [ ] `users` table (Supabase auth integration design)
  - [ ] `agents` table (id, name, system_prompt, tools, config, user_id)
  - [ ] `executions` table (id, agent_id, user_id, prompt, response, cost, latency, created_at)
- [ ] Create migration scripts using Supabase CLI
- [ ] Add database indexes for performance (source lookup, similarity search)
- [ ] Document ER diagram in `docs/database_schema.md`

### Backend Foundation
- [ ] Implement Supabase client configuration
- [ ] Create database models using Pydantic
- [ ] Add basic CRUD operations for `sources`
- [ ] Implement `/sources` POST endpoint accepting `{type, url}`
- [ ] Add `/sources/{id}/status` endpoint
- [ ] Add basic validation and error handling

### Basic Ingestion
- [ ] Implement basic YouTube transcript loader (yt-dlp)
- [ ] Implement basic webpage scraper (BeautifulSoup)
- [ ] Add content preprocessing (cleaning, normalization)
- [ ] Implement simple text chunking (sentence-based, 500 token max)

### Testing
- [ ] Unit tests for database models
- [ ] Integration tests for source CRUD operations
- [ ] Mock tests for basic loaders

## Deliverables
- Complete database schema with migrations
- Basic source ingestion (YouTube + web pages)
- Solid foundation for Week 3 complexity

## Next Steps
Week 03 will add background workers, vector embeddings, and advanced loaders.

## Notes
**Removed from original Week 2:**
- Background workers (moved to Week 3)
- Vector embeddings (moved to Week 3)
- PDF/GitHub loaders (moved to Week 3)
- Complex queue systems (moved to Week 3)

This allows focus on solid database foundations and basic ingestion patterns.
