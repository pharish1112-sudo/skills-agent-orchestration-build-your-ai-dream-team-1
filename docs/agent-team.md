# Agent team for Mona's Project Pulse dashboard

This project uses a custom multi-agent setup orchestrated through GitHub Copilot CLI in a Codespace. The team is defined under the repository's agent folder and each specialist is assigned a clear responsibility for planning, design, implementation, and coordination.

## Team

### 1. Planner
- Model: Claude Opus 5.5 (copilot)
- Responsibility: researches the repository, reads relevant files and documentation, identifies risks and edge cases, and produces an implementation plan with file ownership, dependencies, and validation expectations.
- Definition: `.github/agents/planner.agent.md`

### 2. Designer
- Model: Gemini 3.7 Flash (copilot)
- Responsibility: focuses on UX, accessibility, information hierarchy, interaction flow, and polished dashboard styling for the Project Pulse frontend, while keeping design decisions aligned with the product goals.
- Definition: `.github/agents/designer.agent.md`

### 3. Coder
- Model: GPT-5.5 (copilot)
- Responsibility: implements the actual code changes, fixes bugs, and handles task execution within the scoped files assigned by the orchestrator, including runnable app support when needed.
- Definition: `.github/agents/coder.agent.md`

### 4. Orchestrator
- Model: Claude Opus 5.5 (copilot)
- Responsibility: coordinates the specialist agents, breaks work into phases, assigns file scopes, runs tasks in the correct order, and verifies the integrated result before reporting back.
- Definition: `.github/agents/orchestrator.agent.md`

## How we work together

The Orchestrator manages the workflow by getting a plan from the Planner, delegating design and implementation work to the Designer and Coder, and verifying that the final dashboard hangs together as a coherent Project Pulse experience. This orchestration is performed using GitHub Copilot CLI within a Codespace, which gives the team a structured way to coordinate specialist work without manually mixing responsibilities.
