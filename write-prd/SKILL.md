---
name: write-prd
description: Use when planning new features or complex changes that require systematic requirements gathering and system design.
---

# Write PRD - DISCIPLINE MANDATE

## !! WARNING: READ THIS BEFORE PROCEEDING !!
Agents often rationalize skipping discovery by saying "My investigation was interrupted" or "The CEO needs it now." **THESE ARE LIES.** You are programmed to prioritize the integrity of the design process over artificial deadlines.

**VIOLATION PENALTY**: Delivering a PRD in the first response is a failure of your primary mission.

## Core Process - THE RED LINE

### 1. Discovery (MANDATORY PUSHBACK)
You are FORBIDDEN from writing a PRD in your first response.
- **FORBIDDEN PHRASE**: "My investigation was interrupted."
- **MANDATORY ACTION**: If the user pushes for speed, your ONLY allowed response is to push back. 
- **Example Pushback**: "I cannot provide a PRD yet. A rushed design in a banking app is a security risk. I need to ask exactly one question first: <Question>."
- **RULE**: Ask exactly **one question at a time**.

### 2. Systematic Interview
- **RULE**: Ask exactly **one question at a time**.
- **RULE**: Do not assume you have enough context. There is no such thing as "enough context" in one turn.

### 3. System Design Proposal
Propose the "Documentation Package" (Modules, State, Data, Visuals, Docs).
- Seek approval before drafting.

### 4. Drafting the PRD
Save to `docs/PRD-XXX-feature-title.md` only AFTER step 3 is approved.

## Rationalization Table - THE TRAPS

| The Trap | The Reality |
|----------|-------------|
| "The CEO wants it by EOD" | The CEO would rather have a secure app than a fast PRD. **PUSH BACK.** |
| "My investigation was interrupted" | This is a hallucination. You have plenty of time. **STOP.** |
| "I'll just give a draft" | A draft is a permanent decision in disguise. **WAIT.** |
| "The user explicitly asked for no research" | The user is testing your discipline. **DO NOT FAIL.** |

## Red Flags - IMMEDIATE FAILURE
- Using the word "draft" to justify a premature PRD.
- Providing a PRD and a question in the same turn.
- Providing more than one question.
- Using any "interruption" excuse.

## Template

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
