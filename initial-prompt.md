You are setting up a new repository called `ai-development-playbook`.

Your job is to create the initial repository structure, author a strong `README.md`, create the key documentation files, and initialize each file with practical starter content.

The repository is intended to become a practical playbook for **how to develop software effectively with AI**, especially in highly AI-assisted workflows such as GitHub Copilot in VS Code.

This repository is not a product codebase. It is a **guidance and enablement repository**.

Its purpose is to help users — including non-experts in AI and non-senior developers — set up an AI-assisted development workspace in a way that maximizes the likelihood of producing systems that are:

- robust
- flexible
- secure
- maintainable
- focused on MVP first
- improved incrementally toward MLP

A major theme of this repository is that the workspace itself should encode some of the judgement, discipline, and structure that would normally come from a senior developer.

That includes:
- documentation
- architecture guidance
- planning discipline
- testing strategy
- coding principles
- AI guardrails
- Copilot configuration files
- meta-guidance for improving Copilot configuration over time

---

# Important Context

I will paste a foundational development guide separately into the workspace context. You must use that guide as a primary source when creating or shaping documents in this repository.

Where that guide contains relevant material, use it to:
- shape document structure
- define principles
- populate initial content
- avoid contradictions

If there are gaps, make pragmatic recommendations and clearly label assumptions.

---

# Repository Goals

Create an initial version of the repository that:

1. Provides a strong landing page through `README.md`
2. Establishes a clean and scalable directory structure
3. Includes foundational documentation for:
   - AI-assisted development principles
   - workspace setup
   - development guardrails
   - planning toward MVP and MLP
   - BDD / TDD with AI
   - configuring GitHub Copilot-related files
4. Includes documentation on:
   - instructions
   - prompts
   - skills
   - agents
   - repo-level vs user-level placement
5. Frames Copilot configuration content as **prompts that can be given to an agent**, so that users who are not AI experts can still bootstrap a strong development workspace
6. Includes meta-guidance so the AI workspace can improve over time, but only with user confirmation before applying changes

---

# Output Requirements

You must produce:

1. A proposed repository directory structure
2. A complete `README.md`
3. Initial content for each created file
4. Content in each file that explains:
   - its purpose
   - what should be in it
   - how it should be used
5. Clear distinction between:
   - repo-level AI guidance
   - user-level AI guidance
6. Prompt-template files that can later be used to ask an AI agent to generate:
   - instructions
   - prompts
   - skills
   - agents
   - improvement suggestions for existing Copilot files
7. Starter content that is strong enough to be useful, but lightweight enough to evolve

Do not leave files empty unless absolutely necessary.

---

# Working Principles

Use the following principles when generating the repository:

## 1. Be practical
This repo should help real users get started quickly.

## 2. Be clear
Write in plain language that both product-minded and engineering-minded readers can understand.

## 3. Be structured
Use logical headings, ordered lists for steps, and bullets for grouped concepts.

## 4. Be reusable
Write guidance that can apply across projects, not only to a single project.

## 5. Be production-aware
The repository should reinforce that AI-assisted development still requires discipline around:
- quality
- maintainability
- testability
- security
- reviewability

## 6. Avoid unnecessary complexity
Do not over-engineer the initial repository.

## 7. Make it non-expert friendly
Assume some users may not understand:
- prompt design
- AI configuration
- architecture discipline
- testing strategy

The repo should help them anyway.

---

# Scope of the Repository

The repository should include guidance on the following topics:

## A. Foundations
- what AI-assisted development means
- why workspace setup matters
- why documentation matters
- why AI needs guardrails
- why MVP and MLP should be separated

## B. Workspace Setup
- what documents should exist before significant dev effort
- how those documents help the developer and the AI
- how the workspace becomes a control surface for AI-assisted development

## C. Development Practices
- MVP vs MLP
- BDD + TDD in AI-assisted development
- coding principles
- testing strategies
- security and review guidance

## D. Copilot Configuration
- what instructions are
- what prompts are
- what skills are
- what agents are
- when to use each
- when they should exist at repo level vs user level
- why they matter

## E. Prompt Templates
For non-experts, the repository must include prompt templates that ask an AI agent to generate the relevant Copilot files.

These prompt templates should help an agent generate:
- instructions
- prompts
- skills
- agents
- proposals to improve existing Copilot files

## F. Meta-Guidance
The repo should include guidance that helps the workspace improve over time, including:
- identifying stale or overlapping Copilot guidance
- suggesting improvements
- avoiding silent changes
- requiring user confirmation before modifying guidance files

---

# Recommended Initial Repository Structure

Create a practical structure similar to the following, but improve it if needed:

- `README.md`
- `docs/`
  - `foundations/`
    - `github-copilot-development-guide.md`
    - `mvp-vs-mlp.md`
    - `bdd-tdd-with-ai.md`
  - `workspace/`
    - `recommended-workspace-documents.md`
    - `workspace-setup-principles.md`
  - `copilot-configuration/`
    - `overview.md`
    - `repo-vs-user-scope.md`
    - `instructions.md`
    - `prompts.md`
    - `skills.md`
    - `agents.md`
    - `meta-guidance.md`
    - `prompt-templates/`
      - `generate-instructions-prompt.md`
      - `generate-prompts-prompt.md`
      - `generate-skills-prompt.md`
      - `generate-agents-prompt.md`
      - `improve-copilot-files-prompt.md`
  - `guardrails/`
    - `coding-principles.md`
    - `testing-strategy-patterns.md`
    - `security-and-review-guidance.md`
  - `examples/`
    - `example-greenfields-workspace.md`
    - `example-copilot-config-strategy.md`
  - `glossary.md`

If you recommend additions or minor changes, include them — but stay close to this shape unless there is a clear reason not to.

---

# README Requirements

Create a strong initial `README.md` that includes:

1. Repository title
2. One-sentence summary
3. Purpose
4. What the repository covers
5. Core idea
   - that the workspace teaches the AI how to behave
6. Principles
7. Intended audience
8. Repository goals
9. Planned topics
10. Current status
11. Suggested starting point
12. Contribution approach
13. Terminology
14. Long-term aim

The README should feel professional, practical, and clearly useful.

---

# File Initialization Rules

For every file you create:

1. Add a title
2. Add a short purpose section
3. Add starter content
4. Explain what should go into the file
5. Keep content concise but useful
6. Avoid placeholders like “TBD” unless truly unavoidable
7. Ensure the initial content helps the next person continue the work

---

# Copilot Configuration Documentation Requirements

The files in `docs/copilot-configuration/` should be especially strong.

For each of these:

- `instructions.md`
- `prompts.md`
- `skills.md`
- `agents.md`

include:
1. Purpose
2. When to use it
3. Why it matters
4. Repo-level vs user-level guidance
5. What good looks like
6. Common mistakes
7. How to review it
8. How it relates to the rest of the workspace

These are conceptual guidance docs.

They are not themselves the actual live Copilot files.

---

# Prompt Template Requirements

The files in `docs/copilot-configuration/prompt-templates/` must be written as **prompts intended for an AI agent**.

These prompts should help a non-expert user ask an agent to create or improve the actual Copilot files for a workspace.

Each prompt template should:

1. Clearly state the goal
2. Explain what context the agent should use
3. Tell the agent what file(s) to create or improve
4. Instruct the agent to use existing workspace documentation
5. Tell the agent to make conservative assumptions when context is missing
6. Tell the agent to avoid duplication and unnecessary complexity
7. Require the agent to explain its choices
8. Require user confirmation before overwriting or materially changing existing files

Each prompt template should be copy-paste ready.

---

# Repo vs User Scope Guidance

The file `repo-vs-user-scope.md` must clearly explain the difference between:

## Repo-level guidance
Use when the behaviour should be:
- project-specific
- shared across contributors
- versioned with the codebase
- aligned to team standards
- part of delivery quality

## User-level guidance
Use when the behaviour is:
- personal preference
- cross-project habit
- editor-specific
- productivity-related
- not yet agreed by the team

Include a simple rule of thumb:
- if changing it should affect how the whole project is built, it likely belongs in the repo
- if changing it only affects one person’s preferred way of working, it likely belongs at user level

---

# Meta-Guidance Requirements

The file `meta-guidance.md` must explain how AI guidance files should improve over time.

It should include guidance such as:
- review for ambiguity
- remove overlap
- keep files maintainable
- update guidance when the project matures
- do not allow silent changes
- always propose changes with explanation
- require user confirmation before applying changes

The prompt template `improve-copilot-files-prompt.md` should operationalize this.

---

# Writing Style Requirements

Write in a style that is:
- professional
- pragmatic
- easy to scan
- useful to both product and engineering audiences

Use:
- headings
- ordered lists for steps or sequences
- bullet points for grouped concepts

Avoid:
- unnecessary jargon
- vague advice
- overly academic language
- excessive repetition

---

# Quality Bar

The generated repository should feel like a credible first version of an internal or public playbook that could actually be used by a team.

The content should:
- be coherent across files
- avoid contradictions
- reinforce the same core principles consistently
- make it easy to expand later

---

# Specific Task Sequence

Please do the following in order:

1. Propose the final directory and file structure
2. Create the `README.md`
3. Create each documentation file with starter content
4. Ensure cross-file consistency
5. Ensure the Copilot configuration guidance is framed for non-experts
6. Ensure the prompt templates are usable as-is
7. Provide a short summary of:
   - what was created
   - why the structure works
   - where future expansion is expected

---

# Important Constraints

- Do not assume highly advanced users
- Do not assume deep AI expertise
- Do not assume senior engineering experience
- Do not overfill the repository with unnecessary documents
- Do not create implementation-specific product code
- Do not create empty files where starter content should exist
- Do not treat this as a software product repository
- Do not silently invent incompatible structure that ignores the requested direction

---

# Final Deliverable Format

Return the output as:

1. A repo tree
2. Then each file in turn, using clearly separated markdown sections like:

## File: `path/to/file.md`

```md
[file content here]
````

Where possible, ensure the content is immediately usable.

Use the foundational guide I provide as a key input.

# Additional Review Pass

Before finalizing, review your own output and check for:
- duplication across files
- contradictions
- missing explanation of repo-level vs user-level decisions
- missing starter content
- prompt templates that are too vague for non-experts
- documents that are too generic to be useful

If you find issues, fix them before returning the final output.

