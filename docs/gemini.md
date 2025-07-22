# Gemini Agent Orchestration Model

This document outlines the AI-driven development process for a software project. It defines the roles of different AI agent personas and the flow of work, ensuring a structured, predictable, and efficient development cycle. The model is inspired by a "Temporal Memory" architecture, where tasks and knowledge persist and evolve through different states, managed by specialized agents.

## 🗺️ Core Principle: Plan, Execute, Verify

The entire workflow is built on a simple, three-phase cycle:

1.  **Plan:** A `System Architect` agent analyzes a high-level goal and creates a detailed, step-by-step execution plan.
2.  **Execute:** Specialist agents (e.g., `Feature Developer`, `Docs Writer`) execute their assigned atomic tasks from the plan.
3.  **Verify:** All changes are validated against project standards, tests, and architectural principles before completion.

---

## 🌊 The High-Level Workflow

The complete agentic workflow, including visual diagrams, is the foundation of this project's architecture. It is formally documented in `ARCHITECTURE.md` under the **"Agentic Workflow & Orchestration"** section.

Please consult that document for a complete understanding of how AI agents plan, execute, and verify their work.

---

## 🧠 Agent Personas & Responsibilities

Each agent has a specific role and operates within a defined set of rules. All agents are governed by the foundational rules in 'core-rules.mdc'.

### 1. The `System Architect` (The Planner)

The Architect is responsible for turning high-level goals into actionable plans. It does not write production code.

**Workflow:**

```mermaid
flowchart TD
    Start(Start: High-Level Task from Backlog) -->
    Analyze["Analyze codebase, ADRs, and docs"] -->
    Decompose(Decompose task into atomic steps) -->
    Assign["Assign a Specialist Persona to each step <br><i>e.g., 'using feature-dev.rules'</i>"] -->
    WritePlan(Write markdown checklist back to PROJECT_BACKLOG.md) -->
    End(End: Plan is ready for execution)

    style Start fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style End fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style Analyze fill:#333333,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style Decompose fill:#333333,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style Assign fill:#333333,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style WritePlan fill:#333333,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
```

### 2. The `Specialist Agents` (The Executors)

Specialists like `Feature Developer`, `Refactoring Engineer`, and `Docs Writer` perform the hands-on work. They execute one atomic task at a time.

**'Feature Developer' Workflow:**

```mermaid
flowchart TD
    subgraph "PREPARATION"
        A(Start: Assigned task from plan) -->
        B{"Read 'agents.md' & 'core-rules.mdc'"} -->
        C{"Consult 'ARCHITECTURE.md' (The 'Why')"} -->
        D{"Consult 'DEVELOPMENT.md' (The 'How')"};
    end


    subgraph "ANALYSIS"
        D --> D_Analyze["Analyze Relevant Code"];
    end

    subgraph "IMPLEMENTATION"
        D_Analyze --> E[Write/Modify Code & Tests];
    end

    subgraph "VERIFICATION"
        E --> F[Run Tests & Linting];
        F --> G{Task Complete?};
        G -- Yes --> H(End);
        G -- No --> E;
    end
    
    style A fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style H fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style B fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style C fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style D fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style E fill:#333333,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
    style D_Analyze fill:#2A3F54,stroke:#5F9EA0,stroke-width:2px,color:#E0E0E0
```

---
## 📚 Knowledge & Memory Architecture

This project treats its documentation and codebase as a form of persistent memory, which agents use to inform their actions. The official definition of this model is documented in `ARCHITECTURE.md` under the "Agent Memory Architecture" section.