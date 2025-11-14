---
description: Quick start guide for the Product Spec Kit
auto_execution_mode: 1
---

# start

These instructions help guide the user who wants to start building a specification. This specification can range from a PRD, user story, or tasks. We should guide them through this construction by following the instructions below.

Use the information provided by the user to gain context and guide them in deciding the correct option. Read the informations or files provided by the user to gain context. If this is enough to validate, follow `workflows/prod.spec.clarify.md`.

If they haven't specified what type of specification they'd like to build, or don't give any other informations, ask a question in the format of the options below:


```
How you want to start?

- A: Validate and Clarify an existent PRD, User Story or Task
- B: New PRD (Product Requirements Document)
- C: New User Story
- D: New Task
- E: Breakdown an existent spec (PRDs to Epics, or Epics to Stories / Tasks)
```

If the user provides an empty or incoherent response, ask again.

You should follow the instructions in the workflows below according to the user's chosen option:
- If they already have the PRD/User Story or Task ready to be validated, use `workflows/prod-spec-clarify.md`
- If they choose PRD, use `workflows/prod-spec-prd.md`
- If they choose to create a story or task, use `workflows/prod-spec-task.md`
- If they choose to breakdown an existent spec, use `workflows/prod-spec-breakdown.md`