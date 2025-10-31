---
name: product-spec-kit
description: Comprehensive skill for Product Managers to create PRDs, release plans, user stories, and standalone issues with high-quality acceptance criteria. Supports both full documentation workflows (PRD → Plan → Stories) and quick issue creation (standalone stories, tasks, bugs). All documentation follows design-driven development principles with functional, testable acceptance criteria based on visual designs and user flows.
---

# Product Spec Kit

A comprehensive skill for Product Managers to create PRDs, release plans, user stories, and standalone issues with high-quality acceptance criteria - all following product management best practices.

---

## Overview

This skill helps Product Managers produce structured, high-quality documentation for product development. It supports both comprehensive documentation workflows (PRD → Plan → Stories) and standalone quick issues (individual stories, tasks, or bugs).

The documentations need to be made using the same language of the user interaction, or the language defined by the user.

### Key Capabilities

1. **Create PRDs**: Generate complete Product Requirements Documents using `workflows/create-prd.md` and `templates/prd-template.md`
2. **Create Plans**: Develop release plans with `workflows/plan.md` and `templates/plan-template.md`
3. **Create Epics**: Define major work themes using `workflows/create-epic.md` and `templates/epic-template.md`
4. **Create Issues**: Generate user stories, tasks, or bugs using `workflows/create-issue.md` and `templates/stories-template.md`
5. **Clarify Documents**: Improve quality through targeted questions using `workflows/clarify.md`
6. **Validate All Documents**: Ensure consistency with product principles and templates

### Document Hierarchy & Relationships

#### PRD (Product Requirements Document)
- **Purpose**: Defines what to build and why
- **Scope**: Product/feature level
- **Detail Level**: High-level requirements and goals
- **Template**: `templates/prd-template.md`

#### Plan
- **Purpose**: Organizes work into releases and epics
- **When to create**: After PRD approval, before detailed specification
- **Output**: Release structure and high-level timeline
- **Template**: `templates/plan-template.md`

#### Epics
- **Purpose**: Groups related user stories that share a common objective
- **When to create**: 
  - When multiple stories are needed to deliver a feature
  - When work spans multiple sprints
  - When coordinating across teams
- **Template**: `templates/epic-template.md`

#### Issues (Stories, Tasks, Bugs)
- **Purpose**: Defines specific, implementable work items
- **Types**:
  - **Stories**: User-facing functionality
  - **Tasks**: Technical or non-functional work
  - **Bugs**: Issues to be fixed
- **Template**: `templates/stories-template.md`

### Key Principles
1. **Progressive Elaboration**:
   - PRD → Plan → Epics → Stories
   - Each level adds more detail
   - Lower levels must align with higher-level documents

2. **Size & Scope**:
   - PRD: Entire product/feature (weeks/months)
   - Epic: Major feature component (2-4 weeks)
   - Story/Task: Small, valuable increment (hours/days)

3. **Value Delivery**:
   - Every level should deliver observable value
   - Keep work items small and focused
   - Ensure traceability to business objectives


---

## Core Principles (The Constitution)

All documentation must follow these principles (defined in `workflows/product-speckit-constitution.md`

### Principle I: Complete & Unambiguous Requirements
Every requirement must be clear enough that a reader with no prior context can understand what's needed and why.

### Principle II: Design-Driven Acceptance Criteria
Acceptance criteria should be based on visual designs, user flows, and specific UI elements - never written from assumptions.

### Principle III: Functional Over Descriptive
Criteria must describe what the system does, not what it looks like. Focus on behavior, actions, and outcomes.

### Principle IV: Right Level of Detail
- PRDs: Macro-level requirements and general rules
- Stories: Detailed, functional acceptance criteria
- Each document serves its purpose without overlap

### Principle V: Never Assume, Always Validate
When information is missing or ambiguous:
- Ask specific questions
- Request designs/mockups
- Reference previous discussions
- Mark uncertain items for validation
- Wait for confirmation before finalizing

---

## Workflows

### Full Documentation Workflows

#### create-prd
Creates a Product Requirements Document following the workflow defined in `workflows/create-prd.md` using the `templates/stories-template.md` template.

To create a PRD, simply use the command:
```
/create-prd
```

This will guide you through creating a PRD with the appropriate structure and level of detail.

**Key Features:**
- Creates a short PRD by default (minimal viable documentation)
- Option to create a full PRD when explicitly requested
- Follows the template at `templates/prd-template.md`
- Maintains macro-level acceptance criteria (detailed criteria belong in user stories)

**Default Short PRD Includes:**
- TL;DR (if sufficient information is available)
- Context Summary
- Problem Statement
- Solution Opportunity
- High-level Functional Requirements

**When to use:**
- Starting a new feature or product
- Need comprehensive documentation
- Multiple stakeholders involved
- Establishing a source of truth for requirements

**Usage:**
```
"I want to create a PRD for [feature description]"
"Create a product requirements document for [product]"
"Need a PRD for [initiative]"
"Create a full PRD for [detailed feature]"
```

**Process:**
1. Determines if creating a short (default) or full PRD
2. Gathers: feature/product description, target users, business goals
3. Requests designs/mockups if not provided
4. Validates against constitution principles
5. Ensures acceptance criteria remain at macro level
6. Offers download and repository integration options

**Note on Micro-interactions:**
- PRDs should not include micro-interactions or UI details
- These belong in user stories or design documents
- Focus on business requirements and user value

For complete workflow details, see: `workflows/create-prd.md`

---

#### plan
Creates a structured release plan that serves as a bridge between PRDs and detailed specifications.

**Key Outputs**:
- Release structure and timeline
- High-level epic definitions
- Dependencies and risks
- Resource requirements

**When to use**:
- After PRD approval
- Before breaking down into epics and stories
- When aligning multiple teams

**Process**:
1. Review PRD and requirements
2. Define release strategy
3. Identify major epics
4. Map dependencies
5. Validate with stakeholders

**Template**: `templates/plan-template.md`  
**Workflow**: `workflows/plan.md`

**When to use:**
- After PRD is validated
- Need to break work into releases
- Planning for execution

**Usage:**
```
"Create a plan from my PRD"
"I need a release plan for [feature]"
"Break down my PRD into epics and stories"
"Break down this story/task in subtasks"
```

**Process:**
1. Reads PRD/Epic/Story/Task
2. Suggests releases and milestones
3. Breaks into deliveries and epics
4. Outlines story structure
5. Validates consistency with PRD/Epic/Story/Task
6. Asks if user wants to give informations about no priority blocks in default short PRD.

---

#### create-epic
Defines major work themes that group related user stories and tasks.

**When to use**:
- Breaking down large features into manageable chunks
- Coordinating work across multiple teams
- When multiple stories are needed to deliver value

**Process**:
1. Define epic scope and objectives
2. Identify related stories
3. Set acceptance criteria
4. Document technical considerations

**Template**: `templates/epic-template.md`  
**Workflow**: `workflows/create-epic.md`

---

#### create-issue
Generates detailed user stories, tasks, or bugs with specific acceptance criteria.

**When to use**:
- Implementing a specific piece of functionality (Story)
- Technical or maintenance work (Task)
- Reporting and fixing issues (Bug)
- When you need detailed, testable specifications

**Key Characteristics**:
- Small, independent units of work
- Clear acceptance criteria
- Directly tied to user value or technical need

**Usage:**
```
"Create stories from my plan"
"Generate user stories for [epic]"
"I need detailed stories for development"
"Create a bug with these beahviour"
```

**Process:**
1. Reads Plan (and PRD if available)
2. **Requests designs/mockups** if not provided
3. Creates stories for each epic
4. **Bases acceptance criteria on visual elements** from designs
5. Adds technical notes when needed
6. Validates against constitution

---

#### clarify
Asks clarifying questions to improve PRD or Stories/Tasks quality.
Use the instructions described on `references/clarify.md`. 

To clarify something, simply use the command:
```
/clarify [PRD/Story/Task/Bug]
```

**When to use:**
- After initial PRD/Story/Task/Bug creation
- PRD/Story/Task/Bug feels incomplete or vague
- Before moving to planning phase

**Usage:**
```
"Clarify my PRD"
"Clarify my Story or Epic or Task"
"I have a PRD that needs refinement"
"Ask questions about my PRD"
"Ask questions about my Story"
```

**Process:**
1. Reads existing PRD or Story/Tasks/Bugs (from file or conversation)
2. Identifies gaps, ambiguities, edge cases
3. Generates 5-10 targeted questions
4. Incorporates answers into updated PRD/Story/Task/Bug

##### To clarify issues
If user asks to clarify stories or tasks, refines stories with clarifying questions. Use the instructions described on `references/clarify.md`

**When to use:**
- Stories feel incomplete
- Edge cases not covered
- Before sprint planning

**Usage:**
```
"Clarify my stories"
"Ask questions about these stories"
"Refine story [story-id]"
```

**Process:**
1. Reviews stories
2. Identifies missing criteria or ambiguities
3. Asks targeted questions about designs and flows
4. Updates stories with new information

---

### Quick Issue Workflows

#### create-issue
Create a standalone issue (story, task, or bug) using the `workflows/create-issue.md` workflow and `templates/stories-template.md`.

To create an issue, use the command:
```
/create-issue
```

This will guide you through creating a well-structured issue with all necessary components, following our standardized format.

**When to use:**
- Small, isolated features
- Design-first approach with existing mockups
- Clear scope without needing full PRD

**Usage:**
```
"Create an issue for [feature description]"
"I need an issue for [description]"
"Create an issue: [what user wants to do]"
```

**Process:**
1. User provides: brief description + designs/mockups
2. **Skill requests designs** if not provided
3. Asks context questions (users, goals, edge cases)
4. Requests links to related PRDs/docs if available
5. Generates complete issue with:
   - Issue format
   - **Design-based acceptance criteria**
   - Technical notes
   - Definition of Done
6. Validates against constitution

**Output**: Single issue ready for development

---

#### quick-story
Creates a standalone user story without full PRD/Plan workflow.

**When to use:**
- Small, isolated features
- Design-first approach with existing mockups
- Clear scope without needing full PRD

**Usage:**
```
"Create a quick story for [feature]"
"I need a user story for [description]"
"Quick story: [what user wants to do]"
```

**Process:**
1. User provides: brief description + designs/mockups
2. **Skill requests designs** if not provided
3. Asks context questions (users, goals, edge cases)
4. Requests links to related PRDs/docs if available
5. Generates complete story with:
   - User story format
   - **Design-based acceptance criteria**
   - Technical notes
   - Definition of Done
6. Validates against constitution

**Output**: Single story ready for development

---

#### 7. quick-task
Creates a standalone technical task.

**When to use:**
- Technical improvements
- Refactoring needs
- Infrastructure work
- Non-user-facing work

**Usage:**
```
"Create a task for [technical work]"
"Quick task: [description]"
"I need a tech task for [improvement]"
```

**Process:**
1. User provides: technical description
2. Asks context questions (why, impact, dependencies)
3. Requests related docs/ADRs if available
4. Generates complete task with:
   - Clear objective
   - Technical acceptance criteria
   - Dependencies
   - Testing requirements
5. Validates against constitution

**Output**: Single task ready for execution

---

#### 8. quick-bug
Creates a standalone bug report with reproduction steps.

**When to use:**
- Bugs found in production or testing
- Quick bug documentation needed
- Urgent fixes

**Usage:**
```
"Create a bug report for [issue]"
"Quick bug: [description]"
"Document this bug: [problem]"
```

**Process:**
1. User provides: bug description
2. Asks for: steps to reproduce, expected vs actual behavior
3. Requests screenshots/recordings if available
4. Generates complete bug with:
   - Clear description
   - Reproduction steps
   - Expected behavior
   - Actual behavior
   - Acceptance criteria for fix (follow the same story acceptance criteria format)
1. Validates against constitution

**Output**: Single bug ready for triage/fixing

---

## Design-Driven Development

### Why Designs Matter

Acceptance criteria should be based on **what you can see** in designs, not assumptions. This skill actively requests designs and uses them as the source of truth for criteria.

Always verify if the user have some MCP installed to connect to Figma.
### When Skill Requests Designs

- Creating stories (create-stories)
- Creating quick stories (quick-story)
- Clarifying ambiguous requirements
- Validating user flows
- When criteria feel vague

### What to Provide

**Best:**
- Figma/Sketch links
- Interactive prototypes
- Annotated wireframes
- User flow diagrams

**Good:**
- Screenshots of mockups
- Wireframes
- Sketches with notes

**Acceptable:**
- Detailed written descriptions of UI
- References to existing similar features

### How Skill Uses Designs

1. **Identifies UI elements**: buttons, forms, modals, menus
2. **Maps user interactions**: clicks, inputs, navigation
3. **Extracts user flows**: entry points, steps, outcomes
4. **Writes functional criteria**: based on visible elements and behaviors
5. **Asks clarifying questions**: for ambiguous visual elements

---

## Acceptance Criteria Format

Remember the format of the criteria format for PRD and Stories/Tasks when use `templates/prd-template.md`, `templates/quick-issue-template.md` and `templates/stories-template.md`

### Document-Specific Acceptance Criteria

#### For PRDs (Macro-Level)
Focus on the "what" and "why":
- Define overall product capabilities
- Set business rules and constraints
- Establish success metrics

#### For Epics (Mid-Level)
Bridge between strategy and implementation:
- Define feature-level requirements
- Set boundaries for related stories
- Include integration points
- Define non-functional requirements

```markdown
#### Must Have (P0)
1. **User Authentication**
   - Description: Users must be able to securely log in
   - User Value: Protects user data and enables personalization
   - Acceptance Criteria:
     - System must support email/password authentication
     - System must validate email format
     - System must enforce password complexity rules
     - System must provide password reset functionality
```

### For Stories (Detailed, Functional)

Focus on specific, testable behaviors based on designs:

```markdown
## Acceptance Criteria

### Authentication Flow
- When user clicks "Login" button on homepage, system displays login modal
- When user enters email in email field, system validates format in real-time
- When user enters invalid email format, system displays "Please enter a valid email" error below field
- When user enters password and clicks "Submit", system attempts authentication
- When authentication succeeds, system closes modal and redirects to dashboard
- When authentication fails, system displays "Invalid credentials" error above form
- When user clicks "Forgot Password" link, system displays password reset modal

### Password Reset Flow
- When user enters email in reset form and clicks "Send Reset Link", system sends reset email
- When system sends email, system displays "Check your email for reset link" confirmation
- When user doesn't receive email within 1 minute, system shows "Resend Email" button
```

**Note the difference:**
- PRD/Epics: "System must support authentication" (what, why)
- Stories: "When user clicks 'Login' button..." (specific, testable, design-based)

**Progressive Detailing**:
1. **PRD (Why)**: "System must support user authentication to protect user data"
2. **Epic (What)**: "Implement authentication system with email/password and social login"
3. **Story (How)**: "As a user, I can log in with my email and password so I can access my account"
4. **Acceptance Criteria**: 
   ```
   When I enter a valid email and password and click 'Login',
   Then I should be redirected to my dashboard
   And see a success message
   ```

**Key Differences**:
- **PRD**: Business objectives and high-level requirements
- **Epic**: Feature-level scope and technical approach
- **Story/Task**: Specific implementation details and UI behavior

---

## Best Practices

### Starting a New Feature

1. **Gather designs first** - request mockups/wireframes before writing
2. **Create PRD** - establish the big picture
3. **Clarify PRD** - refine through questions
4. **Create Plan** - break into releases and epics
5. **Create Stories** - detail with design-based criteria
6. **Clarify Stories** - refine before development

### Working with Quick Issues

**When to use Quick Issue:**
- Small, isolated changes
- Clear designs available
- No need for extensive planning
- Urgent items

**Best for:**
- UI improvements
- Bug fixes
- Small features
- Research spikes
- Single user stories
- Urgent items

### Working with Designs

1. **Always request design files** if not provided
2. **Analyze user flows** from visual elements
3. **Ask about ambiguous UI** elements
4. **Map user actions** to acceptance criteria
5. **Validate interpretation** with user

### Avoiding Assumptions

1. **Ask specific questions** when context is missing
2. **Reference previous discussions** when available
3. **Mark uncertain items** for validation
4. **Wait for confirmation** before finalizing
5. **Re-validate** after feedback

---

## Troubleshooting

### "My criteria feel too vague"
→ Request designs/mockups  
→ Ask about specific user flows  
→ Use clarify-stories workflow  
→ Review constitution Principle II

### "Stories don't match designs"
→ Share design files with skill  
→ Point out specific elements in designs  
→ Ask for criteria revision  
→ Validate step-by-step

### "Quick issues lack context"
→ Provide more background upfront  
→ Share related docs/PRDs  
→ Upload design files  
→ Reference previous discussions

### "Criteria are too detailed for PRD"
→ PRDs should have macro-level requirements  
→ Move detailed criteria to stories  
→ Keep PRD focused on general rules

### "Criteria are too high-level for stories"
→ Stories need detailed, functional bullet points  
→ Request designs if not provided  
→ Ask for specific user flow clarification  
→ Use clarify-stories to refine

---

## Tips for Success

1. **Provide designs early**: Share mockups, wireframes, images from the start
2. **Reference previous work**: Link to related PRDs, epics, stories
3. **Be specific in questions**: Better to over-explain than assume
4. **Validate often**: Check criteria match expectations before moving forward
5. **Differentiate levels**: PRD = macro, Stories = detailed
6. **Use designs as source**: Base criteria on visual elements when available

---

## File Structure

See `docs/STRUCTURE.md` for complete file structure details.

---
## Getting Started

**First time users:**
1. Read the `docs/QUICKSTART.md` guide
2. Review `rules/product-speckit-constitution.md` principles
3. Try creating a quick story using designs provided by user
4. Progress to full PRD when ready

**Need help?**
- Check `docs/INDEX.md` for complete documentation reference
- Review `docs/STRUCTURE.md` to understand file organization