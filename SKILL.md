---
name: product-spec-kit
description: Comprehensive skill for Product Managers to create PRDs, release plans, user stories, and standalone issues with high-quality acceptance criteria. Supports both full documentation workflows (PRD → Plan → Stories) and quick issue creation (standalone stories, tasks, bugs). All documentation follows design-driven development principles with functional, testable acceptance criteria based on visual designs and user flows.
---

# Product Spec Kit

A comprehensive skill for Product Managers to create PRDs, release plans, user stories, and standalone issues with high-quality acceptance criteria - all following product management best practices.

---

## Overview

This skill helps Product Managers produce structured, high-quality documentation for product development. It supports both comprehensive documentation workflows (PRD → Plan → Stories) and standalone quick issues (individual stories, tasks, or bugs).

### Key Capabilities

1. **Create PRDs**: Generate complete Product Requirements Documents
2. **Clarify PRDs**: Ask targeted questions to improve PRD quality
3. **Create Plans**: Break PRDs into releases, deliveries, epics, and stories
4. **Create Stories**: Generate detailed user stories with acceptance criteria
5. **Clarify Stories**: Refine stories through targeted questions
6. **Quick Issues**: Create standalone stories, tasks, or bugs without full workflow
7. **Validate All Documents**: Ensure consistency with product principles

### Template files

- PRD structure: `templates/prd-template.md`
- Release plan structure: `templates/plan-template.md`
- User stories structure: `templates/stories-template.md`
- Quick issue structure: `templates/quick-issue-template.md`
- Quality checklist: `templates/checklist-template.md`

### References, Workflows and Commands

- To clarify PRD/Stories/Tasks with questions to find gaps `references/clarify.md`

---

## Core Principles (The Constitution)

All documentation must follow these principles (defined in [constitution.md](references/constitution.md)):

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
Creates a complete Product Requirements Document.
Follow the template `templates/prd-template.md` 

By default, always create a short PRD with these minimal options: 
- TL:DR; (if needed, ask to user these minimal informations)
- Contexto Summary
- Problem Statement
- Solution Opportunity
- Functional Requirements (follow the instructions in `templates/prd-template.md` to see the difference about Requirements in PRD and Stories.)

**When to use:**
- Starting a new feature or product
- Need comprehensive documentation
- Multiple stakeholders involved

**Usage:**
```
"I want to create a PRD for [feature description]"
"Create a product requirements document for [product]"
"Need a PRD for [initiative]"
```

**Process:**
1. Asks for: feature/product description, target users, business goals
2. Requests designs/mockups if not provided
3. Validates against constitution principles
4. Offers download and repository integration options
5. Don't asks micro interactions to create PRD. These micro interactions need to be informed when create stories or tasks.

Avoid Objectives and success metrics with invented texts like "Get 90+ note in Lighthouse Best Practices and Mobile Friendly". Let the user specify the metrics or indicators.

---

#### clarify
Asks clarifying questions to improve PRD or Stories/Tasks quality.
Use the instructions described on `references/clarify.md`

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

#### create-plan
Creates release plan with roadmap, deliveries, epics, and stories.
Follow the template `templates/plan-template` 

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

#### create-stories
Generates detailed user stories with acceptance criteria.
Follow the template `templates/stories-template` 

**When to use:**
- After plan creation
- Ready for development sprint
- Need refined, ready-to-code stories

**Usage:**
```
"Create stories from my plan"
"Generate user stories for [epic]"
"I need detailed stories for development"
```

**Process:**
1. Reads Plan (and PRD if available)
2. **Requests designs/mockups** if not provided
3. Creates stories for each epic
4. **Bases acceptance criteria on visual elements** from designs
5. Adds technical notes when needed
6. Validates against constitution

**Important**: Stories should reference specific UI elements, user flows, and interactions visible in designs.


---

### Quick Issue Workflows

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
   - Acceptance criteria for fix
5. Validates against constitution

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

### For PRDs (Macro-Level)

Focus on general rules and high-level requirements:

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
- PRD: "System must support authentication" (what, why)
- Story: "When user clicks 'Login' button..." (specific, testable, design-based)

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

```
product-spec-kit/
├── SKILL.md                    # This file - main documentation
├── README.md                   # User-facing overview
├── CHANGELOG.md                # Version history
├── templates/
│   ├── prd-template.md        # PRD structure
│   ├── plan-template.md       # Release plan structure
│   ├── stories-template.md    # User stories structure
│   ├── quick-issue-template.md # Quick issue structure
│   └── checklist-template.md  # Quality checklist
├── memory/
│   └── constitution.md        # Core principles (Principles I-V)
├── examples/
│   └── (examples)
└── docs/
    ├── QUICKSTART.md          # Getting started guide
    ├── INSTALL.md             # Installation instructions
    ├── WORKFLOWS.md           # Detailed workflow guide
    ├── INDEX.md               # Master documentation index
    └── STRUCTURE.md           # File structure details
```

---

## Version History

- **v1.0** (2025-10-30): Initial release with full workflow

---

## Getting Started

**First time users:**
1. Read the [QUICKSTART.md](docs/QUICKSTART.md) guide
2. Review [constitution.md](memory/constitution.md) principles
3. Try creating a quick story with designs
4. Progress to full PRD when ready

**Need help?**
- See [WORKFLOWS.md](docs/WORKFLOWS.md) for detailed process guides
- Check [INDEX.md](docs/INDEX.md) for complete documentation reference
- Review [STRUCTURE.md](docs/STRUCTURE.md) to understand file organization