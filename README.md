# Meepo Platform

Meepo is a universal platform for integrating, managing, and orchestrating AI agents across different frameworks and providers. Our platform consists of three key components:

1. **pymeepo**: A universal Python SDK for integrating agents from any framework (LangChain, AutoGen, etc.)
2. **Meepo Cloud**: A managed platform for deploying, orchestrating, and monitoring agent workflows
3. **Language SDKs**: Native SDKs in multiple languages for interacting with Meepo Cloud

## Core Features

- **Universal Integration (pymeepo)**: One SDK to integrate and orchestrate agents from any framework
- **Cloud Platform**: Deploy, manage, and monitor agent workflows at scale
- **Multi-Language Support**: Native SDKs for Python, TypeScript, Go, and more
- **Visual Workflow Builder**: Create complex agent workflows through an intuitive drag-and-drop interface
- **Enterprise Management**: Comprehensive tools for deployment, monitoring, and scaling
- **Marketplace**: Share and discover pre-built workflows, tools, and integrations

## Implementation Status

### Platform MVP
- **Visual Builder**: In Development - Create and manage agent teams visually
- **Agent.ai Integration**: Active Development - Access the agent.ai marketplace
- **Team Management**: In Development - Monitor and control agent teams
- **Query System**: Planned - Natural language team creation

### Future Development
- **pymeepo**: Universal Integration SDK (Planned)
- **Framework Support**: LangChain, AutoGen, etc. (Planned)
- **Language SDKs**: Python, TypeScript, Go (Planned)
- **Enterprise Features**: Advanced management and scaling (Planned)

## Getting Started

### Using the Platform (Coming Soon)
- Visit [platform.meepo.ai](https://platform.meepo.ai) to create an account
- Browse available agents from agent.ai
- Create your first agent team
- Monitor and manage your teams

## Development Timeline

### Phase 1: Core Development (Weeks 1-2)
- **Week 1 (March 1-7, 2025)**: [pymeepo SDK and Agent.ai Integration](mvp_weekly_tasks/week1_mvp.md)
  - Develop minimal pymeepo SDK with agent.ai support
  - Implement AutoGen-based orchestration
  - Create basic agent management system
  - Set up SvelteKit project structure

- **Week 2 (March 8-14, 2025)**: [Visual Builder and Team Management](mvp_weekly_tasks/week2_mvp.md)
  - Create drag-and-drop interface with SvelteKit
  - Implement team creation workflow
  - Add query-based agent spawning
  - Develop monitoring interface

### Phase 2: Platform Development (Weeks 3-4)
- **Week 3 (March 15-21, 2025)**: [Platform Features](mvp_weekly_tasks/week3_mvp.md)
  - Enhance team management capabilities
  - Add advanced monitoring features
  - Implement user authentication
  - Create template system

- **Week 4 (March 22-28, 2025)**: [Release Preparation](mvp_weekly_tasks/week4_mvp.md)
  - Set up Cloudflare Pages deployment
  - Create demo applications
  - Write documentation
  - Launch MVP beta

## Documentation

- [Requirements Document](requirements.md): Detailed platform specifications
- Platform Guide: Using the Meepo Platform (Coming Soon)
- Integration Guide: Framework integration with pymeepo (Planned)
- Examples: Sample workflows and use cases (Planned)

## Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details on how to get involved.

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.
