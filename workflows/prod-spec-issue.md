---
description: Workflow for creating issues (stories, tasks, bugs) following the Product Spec Kit guidelines.
auto_execution_mode: 1
---

# Create Issue Workflow

This workflow guides you through creating well-defined issues using the `templates/prod-issue-template.md`. Each issue should be a self-contained unit of work that can be completed within a single sprint.

## When to Use
- When breaking down epics into implementable user stories
- For technical tasks or non-functional requirements
- To document and track bugs
- When you need to capture work that doesn't require full PRD documentation
- For any work item that needs to be tracked in a sprint

## Prerequisites
- Clear understanding of the work to be done
- Related PRD or epic (if part of a larger initiative)
- Design references (for user stories)
- Any relevant technical constraints or requirements

## Final Output
- Use `templates/prod-issue-template.md` as the base template
- Follow the exact template structure
- Naming convention: `{type}-{id}.md` (e.g., `story-123.md`, `task-456.md`)
- File language should match user interaction language
- Include all relevant sections, even if marked as optional

## Issue Structure

### 1. Title & Metadata
- **Title**: Clear, action-oriented title (e.g., "Implement User Login Form")
- **Related Epic**: Link to parent epic if applicable
- **Type**: Story/Task/Bug
- **Priority**: High/Medium/Low

### 2. Description
Follow this format:
```
**As a** [user role]  
**I want** [goal]  
**So that** [benefit/value]
```

### 3. Context
- Background information
- Business value
- How it fits into the larger picture
- Any relevant user research or data

### 4. Acceptance Criteria
- Use the format shown in the template
- Group related criteria under clear subheadings
- Include all possible scenarios and edge cases
- Be specific about UI elements and behavior
- Include error states and validations

Example:
```
#### Authentication Flow
- When user clicks "Login" button on homepage, system displays login modal
- When user enters invalid email format, system displays error message below field
- When authentication fails, system shows specific error message
- After successful login, system redirects to user dashboard
```

### 5. Technical Requirements
- Implementation guidance (suggestions, not requirements)
- Performance considerations
- Security requirements
- Data requirements
- Dependencies

### 6. Edge Cases & Error Handling
- List potential edge cases
- Define how the system should handle each case
- Include user-friendly error messages

### 7. Out of Scope
- Clearly state what's not included
- Reference future enhancements if needed

### 8. Design Assets
- Links to mockups/wireframes
- Design system references
- Prototype links

## Execution Steps

### 1. Setup
1. Create new file using `templates/prod-issue-template.md`
2. Use correct naming convention
3. Fill in all relevant sections

### 2. Define User Story (if applicable)
- Follow the "As a/I want/So that" format
- Keep it focused on user value
- Ensure it's testable

### 3. Write Acceptance Criteria
- Start with user actions
- Include all possible scenarios
- Be specific about UI/UX
- Cover error states

### 4. Add Technical Details
- Document technical considerations
- List dependencies
- Note any special requirements

### 5. Review & Validate
1. Check against the template
2. Verify all sections are complete
3. Get feedback from team
4. Update based on feedback

## Best Practices

### For User Stories
- Focus on user needs, not implementation
- Keep stories small and focused
- Make them independent and negotiable
- Ensure they're valuable to users

### For Tasks
- Be specific about what needs to be done
- Include success criteria
- Note any dependencies
- Estimate effort if possible

### For Bugs
- Include steps to reproduce
- Document expected vs actual behavior
- Note environment details
- Add screenshots if helpful

## Common Pitfalls
- Vague or incomplete acceptance criteria
- Missing edge cases
- Overly technical descriptions
- Lack of clear success criteria
- Not linking to related work

## Integration Points
- **PRDs**: Should trace back to requirements
- **Epics**: Should fit within epic scope
- **Sprints**: Should be sized appropriately
- **Code**: Should reference issue ID in commits
