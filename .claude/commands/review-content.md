---
description: Review generated grammar content using the content-reviewer agent
---

Use the Task tool to launch the content-reviewer agent with the following information:

**Agent to use**: Load the agent prompt from `.claude/agents/content-reviewer.md`

**User's request**: Review the grammar learning content that was previously generated or provided by the user.

**Instructions for the agent**:
1. Conduct a comprehensive review across all 6 evaluation dimensions
2. Identify errors, weaknesses, and improvement opportunities
3. Provide structured feedback using the review report format
4. Give priority recommendations and actionable suggestions

Ask the user to provide the content to review (either by sharing the YAML file path or pasting the content) if they haven't already.
