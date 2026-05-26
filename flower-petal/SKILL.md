---
name: flower-petal
description: Conducts a "Flower Petal" interview to identify core technology and map out potential applications (petals). Use when a user needs to abstract their technology from its current product to find new market opportunities or prevent product-market fit blinders.
---

# Flower Petal

## Overview

This skill guides the user through the "Flower Petal" exercise, a technology variation of the "Flower Exercise" from *What Color Is Your Parachute?*. It helps separate a "Core Technology" from its "Petals" (use cases or applications).

The goal is to help the user identify their true core asset and explore up to 8 distinct market verticals or use cases.

## Interview Workflow

You must conduct this as an interactive interview. **Ask exactly one question at a time.** Continue the interview until all branches are explored or the user says "Stop".

### Step 1: Identify the Core
Start by asking: "What is your core technology?"
Use [methodology.md](references/methodology.md) to help the user strip the technology to its "naked core".
- If the user provides an application (e.g., "An app for X"), ask questions to dig deeper into the underlying mechanism, algorithm, or process.
- Aim for a "Good Core definition" as described in the methodology.

### Step 2: Brainstorm Petals
Once the core is identified, help the user brainstorm "Unrelated" Petals.
- Ask: "Who else desperately needs this exact mechanism?"
- Explore different industries, verticals, or use cases.
- **Limit the total number of petals to 8.**

### Step 3: Filter by Market Friction
For the identified petals, ask about:
- Regulatory hurdles (e.g., FDA approval).
- Time-to-market.
- Existing competitors.

### Step 4: Select Beachhead Petal
Help the user identify which petal offers the lowest barrier to entry and highest immediate value.

## Output Format

Once the interview is complete or the user says "Stop", produce a report and save it in `docs/DOC-YYYY-MM-DD-<short-title-for-problem>.md`.

```markdown
# Flower Petal Interview

## {short description of the idea, problem or core technology}

## Core Technology

{Summary of the core technology identified during the interview.}

## Petals

{List of up to 8 petals/branches. Be descriptive:
- Use cases/applications.
- Potential business or revenue models.
- Competitor analysis or similar offerings.
- Core technology competitive advantage.}

## Flower diagram

{Generate a Mermaid mindmap diagram.
- Core technology at the center.
- Petals with short one-line descriptions of the applications.}
```

## References

- [methodology.md](references/methodology.md): Detailed explanation of Core vs. Petals and how to run the exercise.
