# Meepo Platform

Meepo is a universal platform for integrating, managing, and orchestrating AI agents across different frameworks and providers. Our platform consists of three key components:

1.  **pymeepo**: A universal Python SDK for integrating agents from any framework (LangChain, AutoGen, etc.)
2.  **Meepo Cloud**: A managed platform for deploying, orchestrating, and monitoring agent workflows
3.  **Language SDKs**: Native SDKs in multiple languages for interacting with Meepo Cloud

## Core Features

-   **Universal Integration (pymeepo)**: One SDK to integrate and orchestrate agents from any framework
-   **Cloud Platform**: Deploy, manage, and monitor agent workflows at scale
-   **Multi-Language Support**: Native SDKs for Python, TypeScript, Go, and more
-   **Visual Workflow Builder**: Create complex agent workflows through an intuitive drag-and-drop interface (Post-MVP)
-   **Enterprise Management**: Comprehensive tools for deployment, monitoring, and scaling
-   **Marketplace**: Share and discover pre-built workflows, tools, and integrations (Post-MVP)

## MVP v0.1.0 Status

The current development focus is on delivering a robust MVP (v0.1.0) of the Meepo Platform. The goal is to provide an end-to-end "vertical slice" of functionality.

### MVP Core Capabilities:
-   **Data Ingestion**: Load data from public sources like YouTube, web pages, PDFs, and GitHub repositories.
-   **RAG & Query**: Ask questions over ingested data via a powerful Retrieval-Augmented Generation pipeline.
-   **Agent Orchestration**: Build and run agents with configurable prompts, tools, and LLMs (OpenAI, Claude, Gemini).
-   **Output Integrations**: Push agent responses to external systems like Twitter, WordPress, Slack, or generic webhooks.
-   **Embeddable Chat UI**: Interact with agents through a real-time, embeddable chat widget.

The project is currently in active development, following a detailed 22-week plan.

## Development Timeline (22 Weeks)

The MVP is being developed across four distinct phases, with buffer weeks for stabilization and testing.

-   **Phase 1: Foundation & RAG (Weeks 1-4)**
    -   Project setup, database design, and core backend/frontend scaffolding.
    -   Building the data ingestion pipeline, vector storage, and retrieval API.
    -   *Goal: A working RAG system.*

-   **Phase 2: Agent System (Weeks 6-10)**
    -   Implementing user authentication, the core agent abstraction, and multi-provider LLM integration.
    -   Adding streaming support, secret management, and responsible AI guardrails.
    -   *Goal: A functional, secure agent execution system.*

-   **Phase 3: Integrations & UI (Weeks 12-15)**
    -   Developing output integrations, OAuth 2.0 flows, and a real-time chat UI.
    -   Creating an embeddable widget and developer SDKs (Python/JS).
    -   *Goal: A complete user-facing application with external connections.*

-   **Phase 4: Production Ready (Weeks 17-21)**
    -   Implementing comprehensive observability (logging, metrics, tracing) and security hardening.
    -   Automating infrastructure (Terraform) and CI/CD pipelines for production deployment.
    -   *Goal: A stable, secure, and scalable production launch.*

For a detailed breakdown, see the [**Full 22-Week Timeline**](weekly_tasks/timeline.md).

## Documentation

-   [**MVP Requirements**](mvp_requirements.md): Detailed requirements for the v0.1.0 release.
-   [**Full Timeline**](weekly_tasks/timeline.md): The complete 22-week development plan.
-   [**Weekly Tasks**](./weekly_tasks/): Granular, JIRA-style tasks for each week of development.
-   [Platform Requirements](requirements.md): The long-term vision and full platform specifications.


## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.
