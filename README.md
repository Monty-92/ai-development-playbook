# AI Development Playbook

A practical playbook for building software with AI while maintaining engineering quality.

## Purpose

This repository captures practical guidance, patterns, and working practices for using AI to support software development in a disciplined and production-aware way.

The goal is to help developers use AI to improve speed and effectiveness without sacrificing:

- robustness
- flexibility
- security
- maintainability
- delivery discipline

This playbook is especially relevant for highly AI-assisted workflows, including so-called “vibe coding”, where the developer relies heavily on AI for ideation, planning, generation, and iteration.

---

## What This Repository Covers

This repository covers two closely related areas:

### 1. Developing software effectively with AI
This includes guidance on:

- workspace setup
- project and feature planning
- MVP to MLP delivery thinking
- documentation-led development
- behaviour-driven and test-driven development
- coding standards, review practices, and quality controls
- security, maintainability, and production-aware delivery

### 2. Configuring the AI workspace itself
This includes guidance on:

- what Copilot instructions, prompts, skills, and agents are
- when and why to create them
- whether they should live at the repository level or user level
- how they should evolve as the project matures
- how to ask an AI agent to generate and improve these files on behalf of the user

A key goal of this repository is to make it possible for a **non-expert in AI or software development** to set up a workspace that gives AI the best chance of producing useful, disciplined, and production-aware outcomes.

---

## Core Idea

In AI-assisted development, the workspace is not just a place to store code.

It is the environment that teaches the AI:

- what is being built
- why it matters
- what good looks like
- what should be avoided
- how quality should be enforced
- how the project should evolve over time

A well-prepared workspace can transfer some of the judgement and discipline of a senior developer into the development process through:

- documentation
- architecture direction
- planning constraints
- testing strategies
- coding principles
- AI guardrails
- Copilot configuration files
- meta-guidance for improving those files over time

---

## Principles

The guidance in this repository is based on the following principles:

1. **Plan before building**
   - define the problem, users, and goals clearly

2. **Constrain scope intentionally**
   - separate MVP from later maturity work

3. **Use documentation as AI context**
   - good documents improve build plans, code suggestions, and consistency

4. **Anchor development in behaviour and tests**
   - use BDD and TDD patterns to reduce drift and ambiguity

5. **Assume AI needs guardrails**
   - do not rely on AI to infer security, robustness, or maintainability requirements

6. **Treat the workspace as a control surface**
   - the structure and guidance in the workspace should shape how AI behaves

7. **Continuously improve the AI setup**
   - refine instructions, prompts, skills, agents, and supporting documents as the project evolves

8. **Keep humans in control**
   - AI may suggest improvements, but meaningful changes to project guidance should be reviewed and confirmed by the user

---

## Intended Audience

This repository is primarily for:

- software engineers
- technical product owners
- engineering leads
- developers learning to work effectively with AI tools
- teams experimenting with AI-assisted software delivery
- non-expert users who want help setting up an AI-ready development workspace

---

## Repository Goals

The goals of this repository are to:

- provide practical guidance for developing with AI
- improve the quality of AI-assisted delivery
- make senior engineering judgement more explicit and reusable
- reduce common failure modes in AI-assisted coding
- show how to structure a workspace so AI behaves more consistently
- explain how Copilot configuration files should be used and maintained
- provide prompt templates that help an agent create those configuration files for the user
- create repeatable patterns that can be used across projects

---

## What Makes This Repository Different

This repository does not only describe how to use AI during development.

It also describes how to **set up the AI workspace itself**, including how to create and improve:

- instructions
- prompts
- skills
- agents
- meta-guidance for maintaining those files

Where possible, these are framed as **prompts that can be passed to an AI agent**, so that users do not need to be experts in prompt writing or AI configuration in order to bootstrap a strong development environment.

This makes the repository useful not only as a guide, but also as a **workspace bootstrap playbook**.

---

## Planned Topics

This repository will evolve over time. Initial and planned areas include:

### Foundations
- AI-assisted development principles
- why workspace setup matters
- how to think about MVP vs MLP
- BDD and TDD in AI-assisted workflows

### Workspace Setup
- recommended documents for greenfields development
- how documentation helps guide AI
- how to structure a workspace for planning and delivery

### Guardrails and Quality
- coding principles
- testing strategy patterns
- security and review guidance
- how to keep AI-generated output production-aware

### Copilot Configuration
- what instructions are
- what prompts are
- what skills are
- what agents are
- when to use each
- repo-level vs user-level placement
- how these should evolve over time

### Prompt Templates
- prompts that ask an AI agent to generate:
  - instructions
  - prompts
  - skills
  - agents
  - suggestions for improving existing Copilot files

### Meta-Guidance
- patterns for improving AI guidance files over time
- how to detect overlap, ambiguity, or stale instructions
- how to require user confirmation before changes are applied

---

## Current Status

This repository is in its initial setup phase.

The first focus is to establish a strong baseline for:

- using GitHub Copilot effectively in VS Code
- structuring a workspace for better AI output
- improving planning and implementation quality through documentation and guardrails
- helping users create and improve Copilot-related workspace files through reusable prompt templates

---

## Suggested Starting Point

If you are using this repository as a reference for a new project, start with the following:

1. Define the problem and target users clearly
2. Document user journeys and use cases
3. Identify MVP scope
4. Separate MLP and later-stage improvements
5. Define architecture direction and constraints
6. Document testing strategy and coding principles
7. Decide which AI guidance belongs in the repository and which belongs at user level
8. Use the prompt templates to ask an agent to generate the initial Copilot files for the workspace
9. Review and refine those files before relying on them

---

## Recommended Usage Model

A practical way to use this repository is:

1. Use the guidance documents to understand the development model
2. Use the workspace setup guidance to structure the project
3. Use the prompt templates to ask an AI agent to create Copilot-related files
4. Review the generated files for clarity, relevance, and scope
5. Improve the workspace incrementally as the project matures

This approach is designed to help teams and individuals create an AI-assisted development environment that remains controlled, understandable, and maintainable.

---

## Contribution Approach

This repository should evolve through practical usage.

Contributions should aim to:

- improve clarity
- reduce ambiguity
- make guidance more actionable
- capture lessons learned from real projects
- keep recommendations grounded in engineering quality
- improve the usefulness of prompt templates for non-experts
- make repo-level vs user-level guidance easier to apply

Contributions should avoid:

- unnecessary complexity
- duplicated guidance across multiple files
- advice that assumes deep AI expertise
- overly abstract recommendations that are hard to apply

---

## Terminology

### AI-Assisted Development
A development approach in which AI tools actively support planning, documentation, implementation, testing, and refinement.

### Workspace
The combination of files, documentation, guidance, and configuration that shapes how development happens in a project.

### MVP
**Minimum Viable Product** — the smallest version of a solution that delivers core value and validates assumptions.

### MLP
**Minimum Lovable Product** — the next stage after MVP, focused on improving usability, resilience, and broader fit.

### BDD
**Behaviour-Driven Development** — defining expected behaviour using user-focused scenarios.

### TDD
**Test-Driven Development** — using tests to guide implementation and verify correctness.

### Instructions
Persistent guidance that shapes how an AI assistant should behave in a workspace.

### Prompts
Reusable task-oriented inputs that ask an AI to perform a specific piece of work.

### Skills
Reusable capability patterns or workflows that package a repeatable type of work.

### Agents
Role-oriented AI configurations or behaviours that operate with a specific responsibility or perspective.

### Repo-Level Guidance
AI guidance that should be versioned with the codebase because it affects how the project is built or maintained by the team.

### User-Level Guidance
AI guidance that reflects an individual’s personal working style, tooling preferences, or cross-project habits.

### Vibe Coding
A highly AI-assisted way of working where the developer relies heavily on AI generation and iteration. In this playbook, the term assumes that strong guardrails are required to keep outcomes production-aware.

---

## Long-Term Aim

The long-term aim of this repository is to help teams use AI as a force multiplier for software development while keeping engineering judgement, quality, and control firmly in place.

Over time, this repository should become a practical reference for:

- setting up AI-ready development workspaces
- improving how developers and teams work with AI
- making good engineering habits easier to encode, reuse, and scale
