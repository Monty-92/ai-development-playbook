Absolutely — below is an **initial version** of the **GitHub Copilot Development Guide**, written as a practical internal guide for **PMs and Engineers**, with emphasis on:

*   setting up a workspace for AI-assisted development
*   keeping Copilot aligned to MVP-first delivery
*   improving robustness, flexibility, and security
*   using documentation and guardrails to transfer senior engineering judgement into the workspace

This version is intentionally **foundational**. It gives you a strong base that can later be expanded with:

*   instruction files
*   prompts
*   skills
*   agents
*   meta-guidance for evolving Copilot files over time

***

# GitHub Copilot Development Guide

## 1. Purpose

This guide defines a practical approach for using **GitHub Copilot in VS Code** to support greenfields development in a disciplined, production-aware way.

The goal is to ensure Copilot is used as more than a coding assistant. It should be guided to support:

*   problem framing
*   scope definition
*   build planning
*   implementation
*   testing
*   iterative improvement

The intended outcome is a workspace that helps a developer build toward a system that is:

*   robust
*   flexible
*   secure
*   maintainable

This is especially important in highly AI-assisted workflows, including so-called **“vibe coding”**, where the developer relies heavily on AI for generation and iteration. In such cases, the workspace must provide the guardrails and structure that would otherwise come from a more experienced engineer.

***

## 2. Core Principle

### The workspace is the control surface

In AI-assisted development, the quality of the output depends heavily on the quality of the workspace context.

A well-prepared workspace should do more than store code. It should communicate:

*   what is being built
*   why it is being built
*   what matters most
*   what must not be done
*   how quality should be measured
*   how the solution should evolve over time

In practice, this means the workspace should encode some of the judgement normally provided by a senior developer through:

*   project documentation
*   architecture notes
*   scope boundaries
*   testing expectations
*   coding principles
*   Copilot guidance files

***

## 3. Objectives of This Guide

This guide aims to help teams use Copilot to:

1.  **Build the right thing first**
    *   keep focus on the actual problem
    *   avoid premature complexity

2.  **Plan before implementing**
    *   define MVP clearly
    *   separate MVP from MLP and later phases

3.  **Improve AI output quality**
    *   provide stable context
    *   reduce drift, inconsistency, and hallucinated features

4.  **Increase delivery quality**
    *   use testing, behavioural scenarios, and clear standards
    *   encourage secure and maintainable implementation patterns

5.  **Create reusable development habits**
    *   establish a repeatable approach for future projects

***

## 4. Recommended Development Approach

The recommended flow for AI-assisted greenfields work is:

1.  Define the problem and target users
2.  Capture user journeys and use cases
3.  Define MVP scope
4.  Define MLP scope
5.  Record architecture direction and constraints
6.  Define behavioural scenarios and testing strategy
7.  Ask Copilot to generate build plans
8.  Implement incrementally with regular review
9.  Refine the workspace guidance as the project evolves

This sequence helps keep Copilot aligned to value, scope, and quality from the start.

***

## 5. Recommended Workspace Structure

The following document set is recommended before significant development begins.

These files provide the context Copilot needs to reason more effectively about the project.

| File                       | Suggested Location    | Purpose (for Developer & Copilot)     | What the Document Should Contain                                                                |
| -------------------------- | --------------------- | ------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `README.md`                | `/`                   | Primary workspace entry point         | Project summary, problem statement, value proposition, links to key docs                        |
| `PRODUCT_BRIEF.md`         | `/docs/product/`      | Defines the “why”                     | Problem statement, target users, goals, non-goals, success criteria                             |
| `USER_JOURNEYS.md`         | `/docs/product/`      | Defines user flow                     | Main journeys, happy paths, alternate flows, failure scenarios                                  |
| `USE_CASES.md`             | `/docs/product/`      | Defines concrete behaviours           | Actor, trigger, preconditions, steps, expected outcome                                          |
| `MVP_SCOPE.md`             | `/docs/planning/`     | Keeps initial delivery focused        | Core features, exclusions, assumptions, MVP acceptance criteria                                 |
| `MLP_SCOPE.md`             | `/docs/planning/`     | Separates later improvements from MVP | Post-MVP features, product enhancements, robustness and usability improvements                  |
| `FEATURE_BREAKDOWN.md`     | `/docs/planning/`     | Enables build sequencing              | Feature decomposition, dependencies, suggested implementation order                             |
| `BUILD_PLAN_MVP.md`        | `/docs/planning/`     | Guides implementation sequencing      | Ordered build steps, checkpoints, definition of done                                            |
| `BUILD_PLAN_MLP.md`        | `/docs/planning/`     | Guides later maturity work            | Follow-on delivery plan, hardening, optimisation, scaling items                                 |
| `ARCHITECTURE_OVERVIEW.md` | `/docs/architecture/` | Provides structural direction         | Components, responsibilities, key boundaries, data flow                                         |
| `TECHNICAL_CONSTRAINTS.md` | `/docs/architecture/` | Prevents invalid solutions            | Approved technologies, infrastructure constraints, security requirements, hosting assumptions   |
| `CODING_STANDARDS.md`      | `/docs/engineering/`  | Improves consistency                  | Naming, formatting, error handling, logging, code organisation principles                       |
| `TESTING_STRATEGY.md`      | `/docs/engineering/`  | Defines quality expectations          | Unit/integration/end-to-end approach, testing priorities, coverage expectations                 |
| `BDD_SCENARIOS.md`         | `/docs/engineering/`  | Grounds development in behaviour      | Given/When/Then scenarios for user-visible behaviour                                            |
| `AI_INSTRUCTIONS.md`       | `/docs/ai/`           | Provides project-specific AI guidance | What Copilot should optimize for, what it should avoid, how it should operate in this workspace |

***

## 6. Why These Documents Matter

Without explicit workspace context, Copilot often defaults to:

*   code-first thinking
*   over-engineering
*   inconsistent assumptions
*   poor prioritisation
*   missing validation and testing

With the right documentation in place, Copilot can better support:

*   build planning
*   feature breakdown
*   scenario generation
*   test creation
*   architecture consistency
*   incremental delivery

These documents do not replace developer judgement. They make that judgement more visible, reusable, and easier for AI to follow.

***

## 7. MVP and MLP Planning

A key discipline in AI-assisted development is separating:

*   **MVP** — the smallest useful version that proves value
*   **MLP** — the next level of maturity once the MVP is validated

Copilot should be guided to build the MVP first.

### MVP should focus on:

*   core user value
*   minimal necessary workflows
*   a narrow but credible solution
*   validation of assumptions

### MLP can then focus on:

*   improved usability
*   stronger resilience
*   broader workflow coverage
*   flexibility and extensibility
*   operational and security hardening

This separation reduces the risk of asking Copilot to solve future problems too early.

***

## 8. Recommended Quality Controls

AI-assisted development should not rely on generation alone. It should be anchored by explicit quality controls.

### Minimum recommended controls

*   documented scope boundaries
*   documented architecture direction
*   coding standards
*   testing strategy
*   behaviour scenarios
*   manual review of AI-generated output

### Strongly recommended controls

*   test-first or behaviour-first development
*   explicit handling of security-sensitive areas
*   clear rules around dependencies and libraries
*   regular review of whether generated code still matches the documented intent

The more autonomy AI is given in generation, the more important these controls become.

***

## 9. BDD + TDD Recommendation

A combined **Behaviour-Driven Development (BDD)** and **Test-Driven Development (TDD)** approach is recommended for AI-assisted development.

### Why this works well with Copilot

It helps keep the workflow anchored to:

*   observable behaviour
*   verifiable outcomes
*   small implementation steps
*   reduced ambiguity

BDD scenarios provide strong guidance for:

*   what the system should do
*   which edge cases matter
*   how user journeys translate into behaviour

TDD helps ensure that:

*   generated code is validated early
*   logic is exercised in a controlled way
*   quality remains part of the workflow, not an afterthought

This combination is especially useful when trying to build something production-worthy with high AI assistance.

***

## 10. Security, Flexibility, and Robustness

One of the biggest risks in AI-assisted development is producing code that appears to work but lacks:

*   security discipline
*   resilience
*   extensibility
*   operational clarity

The workspace should therefore encourage Copilot to build toward production-grade characteristics from the start.

### Robustness

*   clear error handling expectations
*   validation of inputs and outputs
*   test coverage for normal and edge cases

### Flexibility

*   separation of concerns
*   clear component boundaries
*   avoidance of hard-coded assumptions where unnecessary

### Security

*   explicit security requirements in documentation
*   no unsafe assumptions about authentication, authorization, or data handling
*   cautious use of third-party dependencies
*   review of AI-generated code before adoption

Copilot can assist with these areas, but it should not be trusted to infer them reliably without guidance.

***

## 11. Role of the Developer

Even in a heavily AI-assisted workflow, the developer remains responsible for:

*   deciding what should be built
*   evaluating AI output
*   identifying risks and weaknesses
*   validating correctness
*   maintaining quality standards

This guide is not intended to remove judgement from the process. It is intended to make that judgement easier to apply consistently.

In effect, the goal is to make the workspace behave like a lightweight, persistent mentor by embedding:

*   expectations
*   context
*   patterns
*   constraints
*   review criteria

***

## 12. Suggested Working Pattern

A practical pattern for using Copilot in this model is:

1.  Update or refine the relevant workspace documents
2.  Ask Copilot to propose a build plan for the next slice of work
3.  Review the plan against MVP scope and architecture constraints
4.  Ask Copilot to generate scenarios or tests first where appropriate
5.  Implement in small steps
6.  Review generated output for quality, flexibility, and security
7.  Update documentation if the project understanding changes

This creates a feedback loop in which both the code and the workspace guidance improve over time.

***

## 13. Benefits and Risks

### Benefits

*   better alignment between intention and implementation
*   stronger MVP discipline
*   more useful Copilot output
*   improved consistency across the project
*   easier onboarding for less experienced developers
*   more reusable patterns across projects

### Risks

*   workspace documentation becomes stale
*   developers rely too heavily on AI-generated output
*   quality is assumed rather than verified
*   scope grows faster than control mechanisms
*   Copilot configuration is not maintained as the project evolves

These risks should be managed through regular review and deliberate refinement of both the codebase and the workspace guidance.

***

## 14. Future Expansion of This Guide

This initial version focuses on workspace setup and development discipline.

It should later be expanded to include:

*   Copilot instruction files
*   prompts
*   skills
*   agents
*   meta-guidance files that help Copilot identify improvements to its own setup
*   patterns for proposing updates to Copilot files with user confirmation
*   examples of good and bad AI-assisted development workflows
*   templates for new greenfields projects

***

## 15. Target Outcome

The target outcome of this guide is to help developers use GitHub Copilot in a way that increases delivery speed **without sacrificing engineering quality**.

A successful implementation of this approach should result in a workspace that:

*   keeps Copilot focused
*   supports structured planning
*   improves implementation quality
*   increases the likelihood of producing systems that are robust, flexible, and secure

***

## 16. Glossary

### GitHub Copilot

AI-assisted development tooling used within VS Code to support coding, planning, and related tasks.

### Greenfields Development

Starting a new project or product area from scratch rather than extending an existing implementation.

### MVP

**Minimum Viable Product** — the smallest version of a solution that delivers core value and allows early validation.

### MLP

**Minimum Lovable Product** — the next maturity stage after MVP, focused on improving usability, polish, and broader fit.

### BDD

**Behaviour-Driven Development** — an approach that defines system behaviour in terms of user-visible scenarios.

### TDD

**Test-Driven Development** — an approach where tests are written before or alongside implementation to drive design and verify correctness.

### Vibe Coding

A highly AI-assisted style of development in which the developer relies heavily on AI-generated suggestions and iteration. In this guide, the term is used pragmatically and assumes strong workspace guardrails are required to keep the output production-aware.

***

If you want, I can next turn this into either:

1.  a **shorter executive version** for leadership, or
2.  a **practical version 2** that adds:
    *   recommended Copilot files
    *   meta-files
    *   self-improving workspace guidance patterns
