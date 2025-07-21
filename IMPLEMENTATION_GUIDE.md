# Implementation Guide: Adopting Agentic Orchestration Patterns

This guide provides a step-by-step process for applying the patterns from this repository to your own project.

---

## Step 1: Create Your Core Documentation

Create the following three documents in your project's root or a `/docs` directory. Use the generalized files in this repository's `/docs` directory as your template.

1.  **`gemini.md` or `[your_agent_model].md`:**
    *   **Purpose:** Describes the high-level agentic workflow.
    *   **Action:** Copy and adapt `docs/gemini.md` to fit your project's narrative.

2.  **`agents.md`:**
    *   **Purpose:** The main entry point for your AI agents. It maps out the documentation.
    *   **Action:** Copy `docs/agents.md` and, most importantly, update the `[path/to/your/source/code]` placeholder to point to your actual source directory.

3.  **`ARCHITECTURE.md`:**
    *   **Purpose:** The blueprint of your system for your AI.
    *   **Action:** Copy `docs/ARCHITECTURE.md` and fill in the details of your project's architecture, database schema, and API endpoints.

## Step 2: Create Your Agent Execution Rules

This is the most critical part: defining the specific instructions for your AI agents.

1.  **Create a Rules Directory:** Create a `.cursor/rules/` directory in your project root. (The name `.cursor` is a convention from the Cursor IDE, but you can name it whatever your tools require).

2.  **Adapt the Examples:** Review the concrete examples in this repository's `examples/playable-character-cards-rules/.cursor/rules/` directory.

3.  **Write Your Own Rules:** Create your own `.mdc` (or `.md`) files inside your new rules directory. Start by adapting the following core rules:
    *   `core-rules.mdc`: The foundational rules for all agents.
    *   `system-architect.mdc`: The rules for the planning agent.
    *   `feature-dev.mdc`: The rules for the coding agent.

**Crucial:** Your rules files **must contain specific, hardcoded paths and commands** relevant to your project. This is what makes them executable for the AI. Do not use generic placeholders in your own rules.

## Step 3: Integrate with Your AI Tooling

Point your AI development tool (e.g., Cursor, Gemini CLI) to use `agents.md` as the primary entry point and the `.cursor/rules/` directory for its persona-based instructions.

Your AI agents should now be able to follow the Plan, Execute, Verify workflow within your project.
