---
description: Generate, review, and refine grammar units using AI workflow
---

This command orchestrates a multi-agent workflow to create high-quality grammar learning content.

**Workflow Steps:**
1. Read unit list from `present_units.txt`
2. For each unit:
   - **Content Creator Agent** generates initial YAML content
   - Save to `units/unit{N}-*.yaml`
   - **Content Reviewer Agent** reviews the content
   - If critical errors found:
     - **Content Creator Agent** revises based on feedback
     - Save revised version
   - Otherwise, mark as complete

**Instructions for Claude:**

You will execute this workflow step by step. Follow these instructions carefully:

## Step 1: Read Unit List
Read the file `present_units.txt` and parse all units.

## Step 2: Ask User Which Units to Generate
Present the list of units to the user and ask:
- Generate all units? (1-9)
- Generate specific units? (e.g., 1, 3, 5)
- Generate a range? (e.g., 1-3)

## Step 3: For Each Selected Unit

### 3.1 Generate Content
Use the Task tool to launch the content-creator agent:
- Read instructions from `.claude/agents/content-creator.md`
- Provide the unit title (e.g., "Present: Unit1 - am/is/are")
- Save output to `units/unit{N}-{slug}.yaml`
  - Example: `units/unit1-am-is-are.yaml`

### 3.2 Review Content
Use the Task tool to launch the content-reviewer agent:
- Read instructions from `.claude/agents/content-reviewer.md`
- Review the generated YAML file
- Save review report to `reviews/unit{N}-review.md`

### 3.3 Analyze Review Results
Check the review report for:
- Critical errors (🔴)
- Pedagogical concerns (🟠)

### 3.4 Revise if Needed
If critical errors exist:
- Use Task tool to launch content-creator agent again
- Provide:
  - Original unit title
  - Review feedback (critical errors and suggestions)
  - Instruction to revise and fix errors
- Save revised content to same file
- Generate final review (optional)

### 3.5 Report Progress
After each unit, show the user:
- ✅ Unit {N} completed
- 📊 Review rating
- 🔴 Critical errors: {count}
- 🟠 Concerns: {count}
- 📁 Saved to: `units/unit{N}-*.yaml`

## Step 4: Final Summary
When all units are processed, provide:
- Total units generated
- Total with critical errors
- Total revised
- List of all generated files

## Important Notes
- Execute units sequentially, not in parallel
- Wait for each agent to complete before proceeding
- Save all outputs (YAML files and review reports)
- Keep the user informed of progress
- If an agent fails, report the error and ask if you should continue

Begin the workflow now.
