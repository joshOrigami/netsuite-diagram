# netsuite-diagram

[![License: CC-BY-4.0](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Standard: agentskills.io](https://img.shields.io/badge/Standard-agentskills.io-black.svg)](https://agentskills.io)

A deterministic AI constraint layer designed to enforce strict black-and-white architectural documentation for Oracle NetSuite ecosystems using Mermaid.js (`.mmd`) diagrams.

This project provides a specialized, self-contained AI Agent Skill built to be platform-agnostic and fully compatible with the `agentskills.io` open-standard framework.

## The Problem
Generic Large Language Models (LLMs) are notorious for generating "vibe-based" documentation. When tasked with illustrating a NetSuite integration flow or script lifecycle, they default to complex, multicolored layouts using unvalidated structures, missing critical platform limitations, and entirely ignoring the "Unhappy Path." 

In a financial system of record, unverified or outdated documentation creates invisible maintenance liability.

## What This Skill Enforces
When active in your AI-assisted workspace (Cursor, Claude Code, Cline, VS Code extensions), this skill acts as a **Live Control Plane**, forcing your AI assistant to generate technical visuals under rigid engineering constraints:

- **Monochromatic Consistency:** Strictly commands the engine to utilize high-contrast, black-and-white `redux` themes with a standardized `dagre` layout topology. Color styling and gradients are explicitly banned to ensure absolute clean rendering inside Git markdown repositories.
- **Iconography Invariants:** Mandates the exact integration of Google Material bouncer iconography rules across terminal node boundaries:
  - Final terminal success states, data-validation clearances, or successful saves MUST append the `check` (Unicode: ✅ / hex shorthand: `e5ca`) variant.
  - Exception catch blocks, validation failures, or transaction blocks that trigger administrative warnings MUST append the `error` (Unicode: 🛑 / hex shorthand: `e000`) bouncer variant.

---

## Repository Structure

```text
.
├── SKILL.md             <-- The Core Directive (YAML frontmatter + system instructions)
├── README.md            <-- You are here
└── examples/            <-- Reference implementations for AI agent priming (if you wish to add any)
    └── transaction-state-flow.mmd

```

---

## Installation & Setup

### 1. Standalone Integration

To mount this skill directly into your AI context, copy the `SKILL.md` file from this repository and drop it straight into your project's local agent competency folder:

```bash
# For Spec Kit workspaces
mkdir -p .agents/skills/speckit-diagram/
cp path/to/SKILL.md .agents/skills/speckit-diagram/SKILL.md

```

### 2. SDF Extension Pattern

If your development framework leverages automated initialization sequences, embed this asset directly alongside your SuiteCloud project files:

```text
<project-root>/.agents/skills/netsuite-diagram/SKILL.md

```

### 3. Customization

At this point you can edit the `SKILL.md` to alter iconography, color scheme and copyright statements. 

---

## Reference Output Standard

When properly executed by a disciplined AI agent, the resulting design maps out transaction logic flows with high contrast and explicit system boundaries:

```text
---
config:
  layout: dagre
  theme: redux
---
graph TD
    subgraph Platform_Layer [NetSuite Instance]
        UE["User Event: afterSubmit"]
    end

    subgraph Validation_Layer [The Control Plane]
        C1{"Status Check:<br/>Is Invoice Voided?"}
        C2{"Metadata Check:<br/>Field Validated?"}
    end

    subgraph Terminal_States [System Boundary Outcomes]
        SUCCESS["SUCCESS CA ✅<br/>(e5ca / check)"]
        CRASH["TERMINAL FAIL 🛑<br/>(e000 / error)"]
    end

    UE --> C1
    C1 -- "No" --> C2
    C1 -- "Yes (Voided)" --> CRASH
    C2 -- "Valid" --> SUCCESS
    C2 -- "Invalid ID" --> CRASH

```

## Contributing

This is an open-source framework dedicated to establishing true, rigorous engineering standards across the NetSuite community. We highly welcome community pull requests to expand example templates for RESTlet sequences, Map/Reduce stage boundaries, and multi-system webhook routing profiles.

## License

* `SKILL.md` is licensed under the Creative Commons Attribution 4.0 International License (CC-BY-4.0).
* Underlying configuration tools and example files are licensed under the MIT License.

---

*Maintained by Joshua Meiri, Origami Precision, LLC. Built for Always Be Deliberate (ABD) architectural engineering.*
