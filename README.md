# Elephant-Goldfish Model (EGM) in Antigravity

[![Elephant-Goldfish Model](https://img.shields.io/badge/Methodology-Elephant--Goldfish%20Model-1B6EF3)](https://egm.dev)
[![GitHub Repository](https://img.shields.io/badge/GitHub-google%2Felephant--goldfish--model-black?logo=github)](https://github.com/google/elephant-goldfish-model)

This repository is configured to use the **Elephant-Goldfish Model (EGM)** — Google's open-source methodology and plugin for specification-driven development with AI coding agents.

> *"Design with an elephant. Review with a goldfish."*

---

## 🐘 The Metaphor & Core Concepts

When collaborating with AI coding agents on complex engineering projects, long sessions suffer from context drift, confirmation bias, and unstated assumptions. EGM addresses this by dividing responsibilities:

* **🐘 The Elephant (Long-Context Session)**:
  Maintains the continuous, overarching context of your project, product goals, architectural vision, and design iterations. It facilitates brainstorming and drafts formal specifications before code is written.
* **🐟 The Goldfish (Zero-Context Reviewers)**:
  Fresh, isolated subagents spawned without the conversation history that drafted the spec. Reviewing with "fresh eyes," they evaluate design documents, interface contracts, and implementation plans against rigorous engineering rubrics to identify hidden assumptions and blind spots.

---

## 📦 Official Repositories & Resources

* **Upstream Official Repository**: [google/elephant-goldfish-model](https://github.com/google/elephant-goldfish-model)
* **Official Website & Documentation**: [egm.dev](https://egm.dev)
* **Design Standards**: [EGM Document Standards](https://github.com/google/elephant-goldfish-model/tree/main/resources/document_standards)

---

## 🚀 Installed Skills & Workflow Commands

The EGM plugin is installed and ready in this environment via:

```bash
agy plugin install https://github.com/google/elephant-goldfish-model
```

### 1. Ideation & Brainstorming
```text
/egm:egm-brainstorm
```
Engages in structured questioning to refine raw ideas into a coherent hypothesis (`concepts_brief.md`), then stress-tests it with a multi-lens Goldfish critique.

### 2. Drafting Specifications
```text
/egm:egm-draft
```
Converts the concepts brief into a formal markdown design specification saved under `docs/designs/` following the [Feature Specification Standard](https://github.com/google/elephant-goldfish-model/blob/main/resources/document_standards/feature-spec-standard.md).

### 3. Review with Fresh-Context Goldfish Agents
```text
/egm:egm-review docs/designs/<your-spec>.md
```
Spawns fresh, zero-context subagents (Design, Structural, Comprehension, Style, Implementation Readiness) to evaluate your specification.

### 4. Detecting Codebase Drift
```text
/egm:egm-drift-report docs/designs/
```
Compares saved design specifications against the active codebase to detect divergences between intent and code.

### 5. Architectural Bootstrapping
```text
/egm:egm-bootstrap .
```
Discovers repository packages and generates architectural contracts (leaf-level READMEs and rollup blueprints) across your project tree.

---

## 🗂️ Project Structure

```text
.
├── README.md
└── docs/
    └── designs/
        └── example-feature-spec.md  # Starter EGM feature specification template
```
