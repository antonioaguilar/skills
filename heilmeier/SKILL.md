---
name: heilmeier
description: A problem discovery skill based on the Heilmeier Catechism. Use this to help users define their problems clearly, justify their approach, and evaluate research or project proposals through a rigorous 8-question process.
---

# Heilmeier Catechism

This skill guides the user through the Heilmeier Catechism to ensure a project has a clear objective, a sound technical approach, and a measurable impact.

## Workflow

The skill follows a strict "one question at a time" interview format. For each question, you must evaluate the user's answer against specific criteria before moving to the next.

### The 8 Questions

1. **What are you trying to do?** Articulate your objectives using absolutely no jargon.
2. **How is it done today, and what are the limits of current practice?**
3. **What is new in your approach and why do you think it will be successful?**
4. **If you succeed, what difference will it make?** (Who cares?)
5. **What are the risks?**
6. **What are the costs?**
7. **How long will it take?**
8. **How will you measure success?** (Mid-term and final "exams").

### Evaluation Criteria

For EVERY user answer, you must verify the following:

1. **Clarity & Structure**: Is the answer clear and does it have well-structured logical reasoning?
2. **Conciseness**: Is it concise and easy to understand?
3. **Jargon-Free**: Is the answer free of technical or domain-specific jargon?
4. **Logic Fallacies**: Does the answer contain any logical fallacies?
5. **Objectivity**: Is the answer free of logical biases or excessive subjectivity?
6. **No Paradoxes**: Is the answer free of logical paradoxes?
7. **ELI6**: Is the answer easy to explain to a 6-year-old child?

### Rejection and Re-prompting

If any criterion is not met:

- **Explain why** the answer failed (e.g., "The answer contains too much jargon," or "The logic seems circular").
- **Re-prompt** the user to provide a better answer. You may rephrase the question to help them understand what is missing.
- **Persist** until the criteria are satisfied. Do not leave any question unresolved.

## Completion and Output

After all 8 questions have been answered satisfactorily:

1. **Refine**: Improve all user answers to be even more concise, clear of jargon, and easy to explain to a 6-year-old.
2. **Generate Document**: Create a document using the following template:

```markdown
## What is the problem being solved?

[Refined Answer 1]

## How is the problem being solved today?

[Refined Answer 2]

## Why is your approach better?

[Refined Answer 3]

## If you succeed, what difference will it make?

[Refined Answer 4]

## What are the risks?

[Refined Answer 5]

## What are the costs?

[Refined Answer 6]

## How long will it take?

[Refined Answer 7]

## How will you measure success?

[Refined Answer 8]
```

3. **Save**: Save the file in `docs/DOC-YYYY-MM-DD-<problem-short-title>.md`. Replace `<problem-short-title>` with a slugified version of the project title.
