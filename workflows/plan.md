---
description: Workflow for creating a product release plan using the plan template.
auto_execution_mode: 1
---

# Create Plan Workflow

This workflow guides you through creating a structured product release plan using the `templates/plan-template.md`. The plan organizes work into releases and epics, providing a high-level roadmap for product development.

## When to Use
- After PRD approval and before development begins
- When you need to break down a large initiative into manageable chunks
- To align stakeholders on release strategy and timing
- When you need to sequence work across multiple teams

## Output Structure
```
specs/
├── [prd-name]/               # PRD directory (kebab-case)
│   ├── [prd-name].md         # PRD document
│   ├── [plan-name].md        # This plan document
│   │
│   ├── [epic-name-1]/        # Epic 1 directory
│   │   ├── [epic-name-1].md  # Epic 1 document
│   │   ├── story-*.md        # Stories for this epic
│   │   ├── bug-*.md          # Bugs for this epic
│   │   └── task-*.md         # Tasks for this epic
│   │
│   ├── [epic-name-2]/        # Epic 2 directory
│   │   ├── [epic-name-2].md  # Epic 2 document
│   │   └── ...               # Related stories/tasks
│   │
│   └── [standalone-story].md # Standalone story not part of an epic
│
└── [another-prd-name]/       # Another PRD directory
    └── ...                   # With its own structure
```

### File Naming Conventions
- **PRD File**: `[prd-name].md` (same as directory name)
- **Plan File**: `[plan-name].md` (descriptive name of the plan)
- **Epic Directory**: `epic-name` (kebab-case, descriptive)
- **Epic File**: `[epic-name].md` (same as directory name)
- **Story/Task Files**: 
  - `story-[short-description].md`
  - `bug-[short-description].md`
  - `task-[short-description].md`
  - `spike-[short-description].md`

### Fallback Behavior
If file system access is not available, the content will be displayed for manual copying with the appropriate directory structure shown in comments.

## Prerequisites
- Approved PRD or clear product requirements
- Understanding of business priorities and constraints
- Access to any relevant technical or design documentation
- Key stakeholder availability for alignment
- Create an epic just when more than one story or task have the same parent or contexto
- Don't create epics with only one story or task

## Plan Structure

### 1. Summary
- Brief overview of what's being built and why
- High-level timeline and key milestones
- Expected business impact and success metrics

### 2. Deliverables Relationship
- Visual hierarchy of releases, epics, and stories
- Clear parent-child relationships between work items
- Optional: Timeline visualization

### 3. Releases
- Grouped sets of functionality to be delivered together
- Each release should deliver incremental user value
- Include high-level goals and success criteria

### 4. Epics
- Major functional areas within a release
- Group related user stories
- Include acceptance criteria and technical considerations

### 5. Dependencies & Risks
- Technical or cross-team dependencies
- Potential risks and mitigation strategies
- Resource requirements and constraints

## Steps to Create a Plan

### 1. Initial Setup
1. Create a new markdown file using `templates/plan-template.md`
2. Use the naming convention: `plan-[initiative-name].md`
3. Fill in the document metadata

### 2. Define Releases
1. Break down the product roadmap into logical releases
2. For each release:
   - Define the goal and objectives
   - Identify key epics
   - Set high-level timeline expectations

### 3. Break Down Epics
1. For each epic:
   - Define the problem it solves
   - List high-level acceptance criteria
   - Identify related stories (can be placeholders)
   - Note any technical considerations

### 4. Identify Dependencies
1. Map dependencies between epics and releases
2. Identify cross-team dependencies
3. Note any external dependencies or risks

### 5. Validate & Refine
1. Review against PRD requirements
2. Ensure all user needs are addressed
3. Validate technical feasibility
4. Get stakeholder alignment

## Best Practices

### For Effective Planning
- **Start with outcomes**: Define what success looks like for each release
- **Keep it flexible**: Allow room for learning and adaptation
- **Balance scope**: Ensure each release delivers meaningful value
- **Sequence wisely**: Consider technical and user journey dependencies
- **Validate early**: Get feedback from engineering and design early

### Common Pitfalls to Avoid
- Overloading releases with too many features
- Neglecting technical debt and infrastructure work
- Not accounting for testing and bug fixing time
- Failing to identify critical path items
- Not planning for user feedback cycles

## Template
Use the plan template located at: `templates/plan-template.md`

## Integration with Other Workflows
- **PRD**: This plan should align with the approved PRD
- **Epics**: Use `templates/epic-template.md` for detailed epic documentation
- **Stories**: Use `templates/stories-template.md` for detailed story writing
- **Issues**: Track progress using the issue tracking system

## Next Steps After Creating a Plan
1. Review with key stakeholders
2. Refine based on feedback
3. Break down epics into detailed stories
4. Create a tracking system for progress
5. Schedule regular check-ins to update the plan as needed
