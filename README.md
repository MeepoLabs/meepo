# Meepo SDK

Meepo is a powerful SDK for building intelligent agents across multiple programming languages. It provides a flexible, extensible framework for creating, deploying, and orchestrating agents that can leverage various LLM providers.

## Overview

The Meepo SDK enables developers to:

- Build a robust Python SDK with comprehensive agent capabilities
- Access the same functionality in JavaScript/TypeScript, Dart, Go, and other languages via a hosted gateway
- Create sophisticated hierarchical agent structures for complex multi-agent scenarios
- Seamlessly integrate with existing frameworks like LangChain and SmoLAgents
- Leverage multiple LLM providers with unified interfaces and streaming capabilities

## Project Planning

We follow a weekly development cycle with clearly defined tasks and deliverables:

- [Week 1 (March 1-7, 2025)](weekly_tasks/week1.md) - Project Setup and Core Architecture

## Core Features
### Python-First Development

The core SDK is built in Python with:
- Async-first design with synchronous wrappers
- Comprehensive type hints and documentation
- Modular architecture for easy extension
- Robust testing and examples

### Multi-Language Support via Gateway

Access Meepo's capabilities from any language:
- Python SDK for direct integration
- HTTP/WebSocket gateway for other languages
- Thin client libraries for JavaScript/TypeScript, Dart, Go, and more
- Consistent API experience across all languages

### Hierarchical Agent Architecture

Build complex multi-agent systems:
- Supervisor agents that orchestrate and manage other agents
- Worker agents that perform specialized tasks
- Planning agents that break down complex problems
- Validation agents that ensure quality and correctness
- Observer agents that monitor and provide feedback

### Interoperability

Integrate with your existing tools:
- Compatible with LangChain components and agents
- Interoperable with SmoLAgents and other frameworks
- Import/export capabilities for agent definitions
- Bridge adapters for seamless integration

### LLM Provider Integration

Connect to any LLM provider:
- Built-in support for OpenAI, Anthropic Claude, and Google Gemini
- Integration with LiteLLM for expanded provider support
- Custom provider implementations for specialized needs
- Fallback strategies and cost optimization

## Documentation

- [Requirements Document](requirements.md) - Comprehensive requirements and design specifications
- [Examples](examples/) - Example implementations (coming soon)
- [API Reference](docs/) - API documentation (coming soon)

## Getting Started

Coming soon!

## License

This project is licensed under the [GNU General Public License v3.0 (GPLv3)](LICENSE).

## Contributing

Guidelines for contributing to the Meepo SDK will be provided soon.
