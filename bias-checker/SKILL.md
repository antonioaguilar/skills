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
    - For each trigger, write a corrected version of the phrase or sentence that removes the bias while preserving the author's intent.
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

**Correction**:

> **Original**: {the exact phrase or sentence that triggered the bias}
>
> **Corrected**: {the rephrased phrase or sentence with the bias removed}

**Why this works**: {brief explanation of how the rephrasing removes or mitigates the bias}

**Further Reading**: {link / URL to the bias}

## Corrected Text

{the full original text rewritten with all corrections applied}

### Placeholders to fill in

- `{placeholder}`: {what information is needed and where the user can find it}
```

### Notes for the Agent:

- Replace `YYYY-MM-DD` with the current date.
- Replace `short-title` in the filename with a slugified version of the report's short description.
- Ensure each bias entry in the list includes a direct link to its specific page on The Decision Lab if possible (usually `https://thedecisionlab.com/biases/` followed by the hyphenated bias name).
- If multiple biases are found, list them all.
- The **Original** in each correction must quote the trigger verbatim so the user can locate it in their text.
- Corrections must keep the author's meaning and intent; change only what is needed to remove the bias (e.g., replace absolute claims with qualified ones, add missing evidence or alternatives, neutralize loaded language). Do not invent facts.
- If a correction needs information not present in the original text (numbers, dates, names, data sources, criteria), insert a placeholder in the form `{what's needed, where to get it}` instead of inventing a value. Never refer to content that does not exist in the text (e.g., "the criteria below").
- List every placeholder under **Placeholders to fill in** at the end of the report. If no corrections need placeholders, omit that subsection.
- If one sentence triggers several biases, the **Corrected Text** section must apply all of their corrections together so the final text is consistent.
