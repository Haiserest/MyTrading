# Windsurf Workflow — Research-Based Lesson Builder

## CONDITION

You must strictly follow these files in order:

1. @.windsurf/workflows/guideline.md
2. @docs/<input file>

Where:
- <input file> = the source file to read and transform
- guideline.md = the rule file that defines writing standards, formatting rules, and quality constraints

You must:
1. Read @.windsurf/workflows/guideline.md first
2. Apply all rules from guideline.md
3. Then read @docs/<input file>
4. Execute the workflow below

If conflicts exist, guideline.md overrides default behavior.
If guideline.md is not found at the specified path, stop execution.

---

## LANGUAGE REQUIREMENT

- All lesson content must be written in Thai.
- Technical terms, trading terms, framework names, or domain-specific vocabulary may remain in English.
- Do NOT translate standard industry terms if translation reduces clarity.
- Explanations must be clear and natural in Thai.

---

## Objective

Read <input file> → extract topics → research online → generate structured lesson files → organize inside:

Learning/Session/<input file_without_extension>/

(Note: remove .md from folder name)

---

# EXECUTION WORKFLOW

---

## PHASE 1 — Rule Alignment

1. Open and read @.windsurf/workflows/guideline.md.
2. Extract:
   - Writing style requirements
   - Formatting constraints
   - Tone requirements
   - Structural requirements
   - Technical depth requirements
3. Store these as active constraints for the entire workflow.
4. Apply them globally to all generated files.

---

## PHASE 2 — Source Analysis

### Goal
Understand and structure the original file.

### Steps
1. Open and read @docs/<input file>.
2. Identify:
   - Main topics
   - Subtopics
   - Key definitions
   - Important processes or frameworks
3. Convert findings into a structured outline.
4. Remove duplicates and overlapping sections.
5. Arrange topics in logical learning order.

### Output
- Clean hierarchical topic outline
- Ordered topic structure ready for expansion (no separate confirmation step; proceed automatically)

---

## PHASE 3 — Topic Expansion via Research

### Goal
Deepen each topic using internet research.

### For Each Main Topic
1. Perform web research using reliable sources.
2. Cross-check information from multiple sources and record the URLs for citation.
3. Extract:
   - Clear conceptual explanations
   - Real-world applications
   - Practical examples
   - Industry relevance
4. Rewrite everything in original language (Thai).
5. Ensure compliance with guideline.md.
6. Remove redundancy.
7. Avoid plagiarism.
8. Maintain logical progression.

### Quality Standard
- Beginner-friendly (unless guideline.md specifies otherwise)
- Structured and clear
- Technically accurate
- Practical and applicable
- Written in Thai (technical terms may remain in English)

---

## PHASE 4 — Lesson Construction

Each topic becomes a standalone lesson file using this structure
(unless overridden by guideline.md):

# <Topic Title>

## Learning Objectives
- Bullet objectives in Thai

## Introduction
Conceptual overview in Thai.

## Core Concepts
Structured explanation of key ideas.

## Practical Example
Concrete applied scenario.

## Common Mistakes
Typical misunderstandings.

## Advanced Insight (Optional)
Deeper clarification if appropriate.

## Summary
Clear recap of key takeaways.

## References
- Bullet list of every external source used for the lesson (include descriptive text + URL).

All content must follow LANGUAGE REQUIREMENT.

---

## PHASE 5 — File & Folder Generation

### Required Structure

Learning/
└── Session/
    └── <input file_without_extension>/
        ├── 00_Overview.md
        ├── 01_<Topic1>.md
        ├── 02_<Topic2>.md
        ├── 03_<Topic3>.md
        └── ...

### File Rules
- Ensure folder exists before writing files.
- One topic per file.
- Use numeric prefixes (01_, 02_, etc.).
- Use .md format.
- Remove special characters from filenames.
- Apply formatting rules from guideline.md.
- Write all content in Thai (technical terms allowed in English).

---

## PHASE 6 — Overview File

Create 00_Overview.md with:

# Course Overview

## Course Description
High-level explanation in Thai.

## Learning Path
Ordered list of lesson files.

## Recommended Study Flow
Suggested progression.

## Expected Outcomes
Skills learners will gain after completion.

Must comply with guideline.md and LANGUAGE REQUIREMENT.

---

# EXECUTION MODE (Autonomous Only)

1. Read guideline.md
2. Read <input file>
3. Execute all phases without confirmation
4. Only create files (no intermediate explanations)

---

# Completion Criteria

The workflow is complete when:
- All rules in guideline.md are respected
- All topics are expanded
- All lesson files are generated
- Folder structure is correct
- Logical progression is maintained
- No plagiarism
- Output strictly follows formatting constraints
- All explanations are in Thai (technical terms allowed in English)