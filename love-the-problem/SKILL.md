---
name: love-the-problem
description: A problem-first discovery skill based on Ash Maurya's Lean Stack methodology. It helps users detach from solution bias and uncover new product opportunities by identifying the problems created by existing solutions.
---

# Love the Problem, Not Your Solution

This skill guides you through a systematic two-phase interview process to validate the core problem you are solving and identify "unmet needs" in existing market solutions.

## Workflow

The skill follows a strict **"one question at a time"** interview format. You must wait for the user's response before proceeding to the next question.

### Phase 1: Detaching from Solution Bias
The goal of this phase is to move the focus from "what you are building" to "why it needs to exist."

1. **The Initial Hook**: "What is the core solution or product you are currently obsessed with?"
2. **The "Door" Identification**: "If your solution is a 'key,' describe the 'door' (the specific problem) it is meant to open. What exactly happens if this door stays locked?"
3. **The 'Job' Analysis**: "What 'job' is the customer hiring your solution to do? (Focus on the desired outcome, not the features)."
4. **The Monetizable Pain**: "Why is this a 'must-have' problem rather than a 'nice-to-have'? What is the cost of inaction for the user?"
5. **Assumption Stress-Test**: "What is the single biggest assumption you are making about the user's behavior that, if proven wrong, would make your solution irrelevant?"

### Phase 2: Uncovering New Problems in Existing Solutions
New products are often found in the "gaps" or "side effects" of existing products.

1. **Competitive Landscape**: "How are users currently solving this problem (even if it's a 'hack' or a manual process)?"
2. **The 'Original' Success**: "What was the original problem that these existing solutions solved well?"
3. **The 'New' Friction**: "What new set of problems or frustrations has the current solution created for its users? (e.g., Is it too complex? Too expensive? Too slow? Does it require a PhD to use?)"
4. **Unmet Constraints**: "What specific technical or non-technical constraints are preventing existing products from solving these new frustrations?"
5. **The Evolution of the Job**: "How has the user's 'job-to-be-done' evolved since they started using the current solution?"

## Completion and Output

After all questions are answered, synthesize the findings into a document and save it in `docs/DOC-YYYY-MM-DD-<short-title-for-problem>.md`.

### Template:

```markdown
# Problem: {short title for the described problem}

## What is the problem?

[Summary of the problem from the user's perspective, emphasizing the 'door' and the 'job-to-be-done'.]

## Solution bias interview

[List of answers from Phase 1. Document main assumptions, dependencies, and counter-arguments challenging the user's initial solution-focused mindset.]

## Problem discovery interview

[List of answers from Phase 2. Document the original set of problems the existing product solves and the new set of undiscovered problems (limitations, frustrations, unmet features) identified during the systematic process.]
```
