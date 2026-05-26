---
name: write-prd
description: Create a PRD through systematic requirements gathering and system design. Use when planning new features or complex changes.
license: MIT
compatibility: Universal
---

1. **Discovery**: Ask the user for a long, detailed description of the problem they want to solve and any potential ideas for solutions. **Ask exactly one question at a time to keep the focus sharp.** Explore the codebase to verify their assertions and understand the current state of the codebase. **Always read `docs/DOC-terms.md`, `docs/DOC-actors.md` and `docs/DOC-personas.md` (if they exist) to anchor your understanding in the established domain and actors.**

2. **Systematic Gathering**: Interview the user relentlessly about every aspect of this plan until you reach a shared understanding. Walk down each branch of the design tree, resolving dependencies between decisions one-by-one. **Ask exactly one question at a time to keep the focus sharp.**

3. **Module Gathering**: Generate the major modules you will need to build or modify to complete the implementation. Actively look for opportunities to extract deep modules that can be tested in isolation. A deep module (as opposed to a shallow module) is one which encapsulates a lot of functionality in a simple, testable interface which rarely changes. **Ask the user if these modules match their expectations**.

4. **System Design**: Propose a "Documentation Package" including:
   - **Modules**: Outline the major modules needed to build or modify to complete the implementation (from the Module Gathering phase)
   - **State Transitions**: Identify state transitions between the identified modules (deep or shallow) based on the requirements already gathered from the user. Identify complex state transitions that could be relevant to the system or feature design. **Complement this section with a mermaid state diagram as if applicable**
   - **Data Model**: Propose a data model (relational) for the feature discussed.
   - **Visuals**: Propose Mermaid diagrams (Sequence, State, or Flowchart) based on complexity. **Use a sequence diagram as the preferred visual if applicable**
   - **Supporting Docs**: Automatically update or create `docs/DOC-terms.md` (Glossary of terms), `docs/DOC-actors.md` (outline Users and Tasks) and `docs/DOC-personas.md` (these are fictional characters which represent your target users and are created from the `docs/DOC-actors.md`), UX personas include:
     - Profile & Demographics: age group, occupation, and location, technical / non-technical person, tech-savyy / tech illiterate.
     - Behaviors & Motivations: What the user wants to achieve and how they currently interact with your product or similar solutions.
     - Goals & Frustrations: The user's primary objectives and the "pain points" or obstacles that block them from succeeding.
     - Quotes: A short, impactful statement that summarizes the persona's core mindset.

5. **Drafting**: Save the PRD to `docs/PRD-XXX-feature-title.md` using the template below.

<prd-template>

## Problem Statement

The user's pain point and the "why" behind this feature.

## Solution

High-level description of the proposed resolution.

## Success Criteria

Measurable goals that define "done" and "successful" (e.g., performance targets, user behaviors).

## User Stories

A LONG, comprehensive list of user stories in the format:

1. As an <actor>, I want <feature>, so that <benefit>

<user-story-example>
1. As a mobile bank customer, I want to see balance on my accounts, so that I can make better informed decisions about my spending
</user-story-example>

This list of user stories should be extremely extensive and cover all aspects of the feature.

## Implementation Decisions

- **Architecture**: Module boundaries, data flow, and key interfaces.
- **Diagrams**: Embedded Mermaid visuals.
- **Constraints**: Security, performance, or schema requirements.

Do NOT include specific code snippets or file paths.

## Risks & Assumptions

Potential blockers, technical debt, or unverified assumptions made during design.

## Out of Scope

Explicitly excluded items to prevent scope creep.

## Further Notes

Any additional context or future considerations.

## Related PRDs

Links to existing PRDs that this document depends on or interacts with.

</prd-template>
