# Orchestration Patterns for LLM-Powered Agentic Development

This repository is a **template and example collection**, not a library or a framework. It provides a set of documents and concrete examples to help you establish an effective, AI-driven development workflow inspired by a real-world project.

Its purpose is to teach a *pattern* of agentic development that you can adapt to your own projects.

---

## 🤖 Core Philosophy: Plan, Execute, Verify

The workflow is built on a simple, three-phase cycle managed by specialized AI agents:

1.  **Plan:** A `System Architect` agent analyzes a high-level goal and creates a detailed, step-by-step execution plan.
2.  **Execute:** Specialist agents (e.g., `Feature Developer`, `Docs Writer`) execute their assigned atomic tasks from the plan.
3.  **Verify:** All changes are validated against project standards, tests, and architectural principles before completion.

---

## 🚀 How to Use This Repository

1.  **Understand the Philosophy:** Read the documents in the `/docs` directory to understand the high-level concepts, agent roles, and architectural principles.
    *   `docs/gemini.md`: Outlines the overall agentic model.
    *   `docs/agents.md`: Defines the agent personas and the documentation structure they rely on.
    *   `docs/ARCHITECTURE.md`: Provides a template for documenting your system's architecture for AI consumption.

2.  **Review the Concrete Examples:** Explore the `examples/playable-character-cards-rules` directory. This contains the *exact*, unmodified `.cursor/rules/` files from a real project. These files show how the high-level philosophy is translated into specific, executable instructions for an AI agent.

3.  **Adapt to Your Project:** Follow the `IMPLEMENTATION_GUIDE.md` to apply these patterns to your own repository. This will involve creating your own project-specific documentation and agent rules.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
