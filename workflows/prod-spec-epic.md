---
description: Workflow for creating Epics that group related user stories and tasks following the Product Spec Kit guidelines.
auto_execution_mode: 1
---

# Create Epic Workflow

This workflow guides you through creating an Epic using the `templates/prod-epic-template.md`. Epics group related user stories that deliver a significant piece of functionality.

## When to Use
- When breaking down large features into manageable chunks
- When work spans multiple sprints or iterations
- When coordinating work across multiple teams
- For major features or components that need tracking at a higher level
- When you need to group related user stories with a common objective

## Prerequisites
- Existing PRD or product requirements
- Understanding of the target release (if applicable)
- High-level understanding of the technical approach (if available)

## Final Output
- By default, use the `templates/prod-epic-template.md` template
- Follow the template structure exactly as defined
- Name the file using the convention: `{epic-name}-epic.md`
- The final file should be in the same language as the user interaction

## Epic Guidelines
- Focus on the "what" not the "how"
- Each epic should deliver standalone value
- Keep epics to a manageable size (typically 2-4 weeks of work)
- Ensure clear acceptance criteria
- Link to related PRD or parent initiative

## Execution Steps

### 1. Validate Prerequisites
Check if there's an existing PRD or breakdown plan. If not, guide the user to create one first using the appropriate workflow.

### 2. Define Epic Details
1. **Epic Name**: Clear, action-oriented title
2. **Release**: Associated release (if applicable)
3. **Context**: Background and importance
4. **Problem Statement**: What user or business problem this solves
5. **Solution**: High-level approach to solving the problem

### 3. Set Acceptance Criteria
- Define 3-5 high-level acceptance criteria
- Focus on outcomes, not implementation details
- Ensure criteria are testable and measurable
- Base on user needs, not technical details

### 4. Identify Related Stories
- List known user stories that belong to this epic
- Each story should be independently valuable
- Include story IDs and brief descriptions
- Set priorities where possible

### 5. Document Technical Considerations
- Key architecture decisions
- Major dependencies
- Performance considerations
- Security requirements

## Best Practices

### Do
- Keep epics focused on a single objective
- Ensure each epic delivers tangible value
- Make acceptance criteria clear and testable
- Align with product strategy and PRD
- Include relevant stakeholders in review

### Don't
- Make epics too large or too small
- Include implementation details in acceptance criteria
- Forget to link to related PRDs or parent initiatives
- Overlook technical dependencies
- Skip the review process

## Integration with Other Workflows
- **PRD**: Epics should align with product requirements
- **Stories**: Epics will be broken down into multiple user stories
- **Sprints**: Epics typically span multiple sprints
- **Issues**: May generate related tasks or bugs

## Next Steps
After creating an epic:
1. Review with the development team
2. Break down into user stories if not already done
3. Add to your project tracking system
4. Schedule for the appropriate release
