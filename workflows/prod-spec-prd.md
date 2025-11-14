---
description: Workflow for creating a comprehensive Product Requirements Document (PRD) following product management best practices.
auto_execution_mode: 1
---

# Create PRD Workflow

This workflow guides you through creating a complete Product Requirements Document (PRD) following the Product Spec Kit guidelines.

## When to Use
- When starting a new project specification or modifying an existing PRD
- When comprehensive documentation is needed
- When multiple stakeholders are involved
- As a single source of truth for product development and as a basis for deriving stories and tasks
- When product requirements (PRD) are needed for a new feature or product

Always review the non-negotiable rules file at `rules/product-spec-rules` first.
Strictly follow the templates described in the **Final Output** section.

This workflow guides the manager with questions to create or modify specifications such as a Product Requirement Document (PRD). These specifications will be used as a basis for creating project issues (stories, tasks, and bugs) and will also guide code development and its evolutions.

Use the information provided by the user as a starting point. Your goal is to take an initial requirement, deeply understand its rules and expected outcomes, and follow the templates to generate the final file.

Use what the user provides to analyze.

## Final Output
- By default, to create the final file PRD, use the `templates/prod-prd-template.md` template
- **Strictly follow the templates defined here.** Do not create new sections that don't exist in the templates for the final file. Just if the user explicity requests it.
- In the final process, give the final file to the user to validate in markdown format, following the naming convention: `{projectname}-prd.md`
- Only include technical requirements if requested by the user or if they provide this information. Otherwise, leave these requirements out for now.
- The final file language need to be the same language of the user interaction, or the language defined by the user. Including the headings and default content of template.

### General PRD Guidelines
- Be concise but complete
- Use visual aids (diagrams, mockups) when helpful, create them together with the user to ensure they match the desired outcome
- Link to supporting documents instead of duplicating content
- Maintain a single source of truth
- Update the PRD as requirements evolve
- Do not assume or invent data, information, or new sections in the final files

#### Common Pitfalls to Avoid
- Asks questions of clarification phase too soon, when the user doesn't provide enough information. Just follow the PRD template and the rules file. Ask clarification questions just when it's necessary.
- Writing overly detailed requirements (except for stories)
- Not including success metrics
- Failing to validate assumptions
- Not updating the PRD when requirements change
- Creating requirements without user input

## Execution Steps

### Validate Current Requirements
If the user provide an existing PRD, use the existing PRD as a starting point. 

If it doesn't exist, create a new PRD following all the guidelines in this document and the example template.

Review the requirements you've been given and validate that they include all the basic necessary information, which includes:

- WHY we're doing this
- WHAT is being built
- HOW it's being built - less important than the others, but good to have an idea

If the initial requirements aren't sufficient to proceed, ask the user clarifying questions and update the requirements artifact/issue before continuing. Don't assume anything, just ask.

### Acceptance Criteria in PRDs

The acceptance criteria written in a PRD and in Issues (user stories and tasks) are different. In a PRD, the acceptance criteria should be written more broadly, without highlighting user actions or micro-interactions on the platform.

- **Objective**: Define the "what" not the "how"
- **Format**: High-level functionality statements
- **Focus**: Business outcomes and user value
- **Examples**:
  - ✅ "The user can filter search results by price range"
  - ✅ "System validates user email format during registration"
  - ❌ Avoid: "Show error message in red below the email field"

**What to avoid in PRD acceptance criteria**
- Implementation details
- UI/UX specifics (belong in design documents)
- Technical specifications
- Micro-interactions (except for user stories)

### Build Your Understanding of Key PRD Elements:

1. **TL;DR**: Brief summary in three main points and subpoints:
    - **Why** solve
        - [sub-item 1]
        - [sub-item 2]
        - [sub-item 3]
    - **What** to solve 
        - [sub-item 1]
        - [sub-item 2]
        - [sub-item 3]
    - **How** to solve
        - [sub-item 1]
        - [sub-item 2]
        - [sub-item 3]
    - **Context Summary**: Client history and objectives. Expand the WHY from the TL;DR
    - **Problem Statement**: Clear definition of the problem. Extend the problem from the WHY in the TL;DR
    - **Solution Opportunity**: High-level overview of the solution, expanding the WHAT and HOW from the TL;DR
    - **Functional and Non-Functional Requirements**: Only user behaviors and high-level features... No micro-actions or interactions, and no non-functional requirements
    - **Next Evolutions**: Describe what we won't deliver now but is planned for the future.
2. Present your understanding to the user, along with any needed clarifications. Iterate on this until you have 100% clarity.
3. After the user approves your vision, you should edit the file, enhancing it with what was discovered.
4. Check the project rules to identify if there are any main points to follow or if this request violates any main rule or process. If it does, ask for clarification. Only proceed if the user requests it.


## Next Steps
Validate the final content. After PRD approval, create and give the final file to the user. And, give the next steps options:
1. Clarifying and identifying gaps that might be missing from the final PRD using the `prod-clarify.md`
2. Creating a breakdown of requirements into user epics and user stories using the `prod-plan.md` workflow
3. Create epics using `prod-spec-epic.md`
