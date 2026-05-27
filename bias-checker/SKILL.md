---
name: bias-checker
description: Analyzes text or prompts for cognitive biases and provides a detailed report on findings, implications, and references. Use this to identify biases in thinking and improve reasoning.
---

# Bias Checker

This skill analyzes a piece of text, phrase, or prompt to identify cognitive biases. It informs the user about biases found in their thinking and the implications of those biases.

## Workflow

1.  **Input Collection**: Prompt the user for the text or phrase they would like to analyze.
2.  **Analysis**:
    - Examine the provided text for cognitive biases listed in [biases.md](references/biases.md).
    - Identify specific sentences, locations, or phrases that trigger each bias.
    - For each identified bias, determine its description, explanation, and implications.
3.  **Reporting**: Generate a report in the specified markdown format.

## Reference Material

Refer to [biases.md](references/biases.md) for a comprehensive list of biases and their descriptions. This data is based on [The Decision Lab](https://thedecisionlab.com/biases).

## Termination and Output

Produce a report and save it in `docs/DOC-YYYY-MM-DD-bias-report-short-title.md` using the following format:

```markdown
# Bias Report

## {short description }

## Summary

Provide a short summary of the biases found in the user's thinking and fallacies in their logic or reasoning

## List of biases

We found N biases in the {text / paragraph / prompt / information / document} you provided.

### 1. Bias: {name of the bias}

**Trigger**: {what phrase, text or sentence triggered the bias}

**Description & Explanation**: {description and explanation of the bias}

**Implications**: {implications and consequences of the bias}

**Further Reading**: {link / URL to the bias}
```

### Notes for the Agent:

- Replace `YYYY-MM-DD` with the current date.
- Replace `short-title` in the filename with a slugified version of the report's short description.
- Ensure each bias entry in the list includes a direct link to its specific page on The Decision Lab if possible (usually `https://thedecisionlab.com/biases/` followed by the hyphenated bias name).
- If multiple biases are found, list them all.
