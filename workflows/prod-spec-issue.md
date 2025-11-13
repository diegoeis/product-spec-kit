---
description: Workflow for creating standalone issues (stories, tasks, or bugs) using the stories template.
auto_execution_mode: 1
---

# Create Issue Workflow

This workflow guides you through creating issues (story, task, or bug) related or not related with a PRD. Use the `templates/stories-template.md` template. You also can create a single, self-contained piece of work without going through the full PRD process.

## When to Use
- Creating a single user story outside of a full feature
- Creating a series of user stories or tasks related with a PRD and Epics
- Documenting a bug that needs to be fixed
- Creating a technical or non-functional task
- When you need to quickly capture work without full documentation

## Output
- **File Location**: 
  - For epic-related issues: `specs/[prd-name]/[epic-name]/[issue-type]-[short-description].md`
  - For standalone issues: `specs/[prd-name]/[issue-type]-[short-description].md`
- **Directory Structure**:
  ```
  specs/
  └── [prd-name]/
      │
      ├── [epic-name-1]/        # If part of an epic
      │   ├── [epic-name-1].md  # Epic document
      │   ├── story-*.md        # User stories
      │   ├── bug-*.md          # Bug reports
      │   └── task-*.md         # Technical tasks
      │
      └── story-standalone.md   # If not part of an epic
  ```
- **Fallback**: If file system access is not available, the issue content will be displayed for manual copying
- **Naming Conventions**:
  - **User Stories**: `story-short-description.md` (e.g., `story-user-login.md`)
  - **Bug Reports**: `bug-short-description.md` (e.g., `bug-login-error.md`)
  - **Technical Tasks**: `task-short-description.md` (e.g., `task-update-dependencies.md`)
  - **Research Spikes**: `spike-topic.md` (e.g., `spike-auth-providers.md`)

## Prerequisites
- Basic understanding of the issue to be created
- Any relevant context or background information
- Design references (if applicable)

## Issue Types

### User Story
For new functionality or features that deliver user value:
- Includes detailed acceptance criteria
- Links to designs or mockups when available

### Task
For technical or non-functional work:
- Clear description of what needs to be done
- Any technical requirements or constraints
- Dependencies on other work

### Bug
For reporting issues:
- Clear steps to reproduce
- Expected vs. actual behavior
- Environment details (if relevant)

## Steps

### 1. Initial Setup
1. Create a new markdown file using the stories template
2. Use the following naming convention: 
   - For stories: `story-[short-description].md`
   - For tasks: `task-[short-description].md`
   - For bugs: `bug-[short-description].md`
3. Add the appropriate metadata at the top of the file

### 2. Core Components
Fill in these essential sections:

#### Title & Context
- Clear, action-oriented title
- Link to related epic or feature (if applicable)
- Background and business context
- User story format (for user-facing changes)

#### Acceptance Criteria
For issues, acceptance criteria must be more granular than in PRDs, specifying exact user behavior and layout actions. Follow these guidelines:

1. **User Actions & System Responses**:
   - Start with "When [user action], then [system response]"
   - Specify exact UI elements and their behavior journey
   - Include all possible user paths and error states

2. **Layout & Interaction Details**:
   - Reference specific UI components and their states
   - Include validation rules and messages
   - Specify any animations or transitions

3. **Example**:
   ```
   ##### Login Form
   - When user clicks 'Login' button with empty fields, show "Please fill in all required fields" below the form
   - When user enters an invalid email format, show "Please enter a valid email" below the email field immediately after moving focus away
   - When login fails, show error message in red banner at top of form with retry button
   - After successful login, redirect to dashboard with fade-out animation
   ```

4. **Validation Rules**:
   - All interactive elements must be covered
   - Include all error states and validations
   - Specify any loading states or progress indicators

#### Technical Notes (if applicable)
- Implementation considerations
- Dependencies
- Performance or security implications

### 3. Validation
1. Review against the Product Documentation Constitution:
   - Is the purpose and value clear? (Principle I)
   - Are acceptance criteria based on designs? (Principle II)
   - Does it focus on functionality rather than description? (Principle III)
   - Is the level of detail appropriate? (Principle IV)
   - Have all assumptions been validated? (Principle V)
2. Get feedback from team members if needed
3. Update the issue based on feedback

## Best Practices for Issue Acceptance Criteria

### Writing Effective Criteria
- **Be specific and concrete**:
  - ❌ "The form should validate input"
  - ✅ "When user submits the form with an invalid email, show 'Please enter a valid email' in red below the email field"

- **Cover all scenarios**:
  - Happy path
  - Error conditions
  - Edge cases
  - Empty/initial states

- **Reference UI elements precisely**:
  - Use exact field labels and button text
  - Specify locations (e.g., "below the form", "in a red banner at the top")
  - Include any visual feedback (e.g., "show loading spinner", "display success checkmark")

### Common Patterns
1. **Form Interactions**:
   - Field-level validations
   - Form submission handling
   - Error message display
   - Success states

2. **Navigation**:
   - Button/link actions
   - Page transitions
   - Back/forward behavior

3. **Dynamic Content**:
   - Loading states
   - Empty states
   - Error states
   - Data refresh behavior

### Validation Checklist
- [ ] Every user action has a defined system response
- [ ] All UI states are accounted for
- [ ] Error messages are specified with exact text
- [ ] Navigation behavior is clearly defined
- [ ] All interactive elements have specified behavior

## Template
Use the stories template located at: `templates/stories-template.md`

## Common Pitfalls to Avoid
- Creating issues that are too large (break them down)
- Missing acceptance criteria
- Not including necessary context
- Forgetting to link to related work
- Being too prescriptive about implementation details
