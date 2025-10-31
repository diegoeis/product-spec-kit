---
description: Workflow for creating Epics that group related user stories and tasks.
auto_execution_mode: 1
---

# Create Epic Workflow

This workflow guides you through creating an Epic using the `templates/epic-template.md`. Epics represent large bodies of work that can be broken down into smaller, more manageable user stories and tasks.

## When to Create an Epic
- When you have multiple related user stories that share a common goal
- For major features or components that span multiple sprints
- When work needs to be tracked at a higher level than individual stories
- When coordinating work across multiple teams

## Prerequisites
- Clear understanding of the feature or functionality
- Related PRD or product requirements
- Knowledge of the target release (if applicable)
- List of potential user stories or tasks (if available)

## Epic Structure

### 1. Epic Overview
- **Name**: Clear, action-oriented title
- **Release**: Associated release (if applicable)
- **Context**: Background and business value
- **Problem Statement**: What user or business problem this epic solves

### 2. Acceptance Criteria
- High-level criteria that must be met for the epic to be considered complete
- Focus on outcomes rather than implementation details
- Should be testable and measurable

### 3. Related Stories
- List of user stories that make up this epic
- Each story should be independently valuable
- Include priority and brief description

### 4. Technical Considerations
- Architecture decisions
- Dependencies
- Performance requirements
- Security considerations

## Steps to Create an Epic

### 1. Initial Setup
1. Create a new markdown file using `templates/epic-template.md`
2. Use the naming convention: `epic-[short-descriptive-name].md`
3. Fill in the basic metadata

### 2. Define the Epic
1. Write a clear, concise name
2. Add context and background
3. Define the problem statement
4. Link to related PRD or parent epic

### 3. Set Acceptance Criteria
1. Define 3-5 high-level acceptance criteria
2. Ensure they are outcome-focused
3. Make them testable

### 4. Identify Related Stories
1. List all known user stories
2. For each story:
   - Write a brief description
   - Set priority
   - Note any dependencies

### 5. Add Technical Details
1. Document technical approach
2. Note any architectural decisions
3. List dependencies and constraints

## Best Practices

### For Effective Epics
- **Keep them focused**: Each epic should have a single, clear objective
- **Deliver value**: Every epic should deliver tangible user or business value
- **Right size**: Should take 2-4 weeks to complete
- **Testable**: Clear criteria for when the epic is done
- **Aligned with strategy**: Supports product vision and goals

### Common Pitfalls to Avoid
- Creating epics that are too large (break them down)
- Not linking to related PRDs or parent initiatives
- Vague acceptance criteria
- Not identifying all related stories
- Forgetting technical dependencies

## Template
Use the epic template located at: `templates/epic-template.md`

## Integration with Other Workflows
- **PRD**: Should align with product requirements
- **Plan**: Should fit into the overall release plan
- **Stories**: Will be broken down into multiple user stories
- **Issues**: May generate tasks or bugs during implementation

## Next Steps After Creating an Epic
1. Review with the development team
2. Break down into user stories if not already done
3. Add to your project tracking system
4. Schedule for the appropriate release
5. Update the release plan if needed
