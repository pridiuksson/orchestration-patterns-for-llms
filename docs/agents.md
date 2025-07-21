# Agents Guide: The Single Entry Point

**Purpose**: This is the master index for a project using an agentic development model. It is the **only file an AI agent needs to read first**. It contains no implementation details, only pointers to the authoritative documentation.

---

## 🗺️ **Project Documentation Map**

### **Tier 1: Core Guides**
*   **`DEVELOPMENT.md`**: The "How-To" Manual
    *   **Content**: All commands, setup, workflows, and troubleshooting.
    *   **Use When**: You need to build, test, or run the project.

*   **`ARCHITECTURE.md`**: The "What & Why" Blueprint
    *   **Content**: System overview, core principles, and design philosophies.
    *   **Use When**: You need to understand how the system works or why it was designed a certain way.

*   **`PROJECT_BACKLOG.md`**: The "What's Next" Roadmap
    *   **Content**: Prioritized features and execution plans.
    *   **Use When**: You are starting a new development task.

### **Tier 2: Detailed References**
*   **`/ADR` Directory**: The "Legal Code"
    *   **Content**: Detailed, atomic architectural decision records.
    *   **Use When**: You need the specific rationale for a critical implementation pattern.

*   **`[path/to/your/source/code]` Directory**: The "Source of Truth"
    *   **Content**: The working implementation of all backend code.
    *   **Use When**: You need to see the authoritative code for any feature.

---

## 🤖 **Agent Operating Model**

All AI agents in this project operate under a defined set of principles to ensure consistency and efficiency.

*   **Memory Architecture:** The agent memory model is formally defined in `ARCHITECTURE.md` under the "Agent Memory Architecture" section.
*   **Core Protocol:** The foundational behaviors for all agents are defined in `.cursor/rules/operational-protocol.mdc`.

---

## 🚨 **Critical Rules (Non-Negotiable)**

1.  **Start Here**: Always begin by consulting this file.
2.  **Follow Pointers**: Do not look for implementation details here; follow the links.
3.  **Trust the Hierarchy**: The documentation is structured to guide you. `DEVELOPMENT.md` is for "how," `ARCHITECTURE.md` is for "why."
4.  **Code is Truth**: When in doubt, the implementation in the `[path/to/your/source/code]` directory is the final authority.
