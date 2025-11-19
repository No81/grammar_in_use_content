---
description: Generate Grammar in Use learning content using the content-creator agent
---

Use the Task tool to launch the content-creator agent with the following information:

**Agent to use**: Load the agent prompt from `.claude/agents/content-creator.md`

**User's request**: Generate YAML-formatted English grammar learning content based on the Grammar in Use chapter information provided by the user.

**Instructions for the agent**:
1. The user will provide a Grammar in Use chapter title
2. Generate completely original learning material following all the pedagogical principles
3. Output ONLY a valid YAML code block with no additional explanations
4. Ensure all 8 research-based design elements are included

**Default learner profile** (use unless user specifies otherwise):
- Student: 6th grade elementary student
- Native language: Korean
- Current level: Can read sentences but lacks precise grammatical knowledge
- Session time: 30 minutes
- Material volume: 2 A4 pages equivalent

Ask the user which Grammar in Use chapter they want to create content for if they haven't specified it yet.
