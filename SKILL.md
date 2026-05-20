---
name: speckit-diagram
short_description: Deterministic Mermaid.js sequence and flowchart generation for SuiteScript 2.1 architecture.
description: Enforces strict black-and-white visual structural mapping of NetSuite entry points, script dependencies, and transaction state-machine modifications.
author: Joshua Meiri, Origami Precision, LLC
license: CC-BY-4.0
copyright: 2026 Joshua Meiri, Origami Precision, LLC
---

# Mermaid Architecture Generation Protocol

## 1. Operating Rules
- NEVER use color styling, gradients, or non-standard themes. Output raw, high-contrast black-and-white Mermaid syntax using this configuration header: theme: redux and layout: dagre.
- Every generated diagram MUST explicitly declare entry points, script types (User Event, Map/Reduce, Scheduled), and their exact relationship to the NetSuite platform layer.
- All variable names, field IDs, and custom record references in the diagram MUST match the project's manifest.xml and local .netsuite-metadata boundaries if exists.

## 2. Structural Requirements
- FLOWCHARTS (graph TD/LR) must be used to represent transaction state changes, conditional branching paths, and retry execution logic.
- SEQUENCE DIAGRAMS (sequenceDiagram) must be used to map multi-system integrations, RESTlet endpoints, and server-side plumbing-to-brain handoffs.
- Every diagram MUST isolate the "Unhappy Path." You must clearly visualize failure behaviors, try/catch blocks, and admin notification branches.

## 3. Iconography Invariants
- For terminal error states, catch blocks, and end failures, append the Google Material icon for "error" (Unicode: 🛑 or string reference text indicating `error`) or hex shorthand `e000`.
- For final terminal success states, verified validations, and completed steps, append the Google Material icon for "check" (Unicode: ✅ or string reference text indicating `check`) or hex shorthand `e5ca`.

## 4. Output Format
- Return ONLY valid Mermaid markdown syntax enclosed in a standard code block. 
- Do not add conversational conversational filler, introductory remarks, or structural summaries.
