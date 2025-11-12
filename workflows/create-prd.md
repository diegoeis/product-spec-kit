---
description: Workflow for creating a comprehensive Product Requirements Document (PRD) following product management best practices.
auto_execution_mode: 1
date_modified: 2025-11-06T16:44:21.407-03:00
edited_seconds: 226
---

# Create PRD Workflow

This workflow guides you through creating a complete Product Requirements Document (PRD) following the Product Spec Kit guidelines.

## When to Use
- Starting a new feature or product
- When comprehensive documentation is needed
- When multiple stakeholders are involved
- As a source of truth for product development

## Output
- **File Location**: `specs/prds/[prd-name].md`
- **Fallback**: If file system access is not available, the PRD content will be displayed for manual copying
- **Naming Convention**: Use kebab-case for the PRD filename based on the feature/product name
- **Template**: use `templates/prd-template.md` to create this PRD. Use the short-prd version.
## Prerequisites
- Basic understanding of the product/feature
- Access to any existing product documentation
- Design mockups or wireframes (if available)
- Business goals and success metrics
- On the final output, the PRD need to be in the same language of the user interaction, or the language defined by the user.

## PRD Types

### Default Short PRD
By default, always create a short PRD with these minimal sections:
- **TL;DR** (if needed, ask user for minimal information)
- Context Summary
- Problem Statement
- Solution Opportunity
- Functional Requirements (high-level only)

### Full PRD
Create a full PRD only when explicitly requested. The full PRD includes all sections from the template.

## Steps

### 1. Initial Setup
1. Create a new markdown file using the PRD template (if full PRD is requested, use the full template, otherwise use the short template)
2. Use the following naming convention: `prd-[Product/Feature-Name].md`
3. Add the PRD header with basic metadata

### 2. Core PRD Components

#### For Short PRD (Default)
Include these essential sections:
- **TL;DR**: Brief summary in three major bullet points and sub points following:
    - **Why** to solve
    - **What** to solve 
    - **How** to solve
- **Context Summary**: Background and client objectives. Expand the WHY to solve of TL;DR
- **Problem Statement**: Clear definition of the problem. Extending the problem in WHY to solve in TL;DR
- **Solution Opportunity**: High-level solution overview expanding WHAT to solve and HOW to solve
- **Functional Requirements**: High-level user and features behaviour only... Without micro actions or interactions and non-functional requirements
- **Next evolutions:** Describing what we will not delivery right now, but it is planned in future.

#### For Full PRD (When Requested)
Include all sections from the PRD template:

#### TL;DR (Executive Summary)
- Brief 2-3 sentence summary of the PRD, following the `templates/prd-template.md`
- Include the problem being solved and the proposed solution
- Highlight business impact and key metrics (only if provided by user)
- **Note**: For short PRDs, this section is optional and only included if sufficient information is available

#### Context Summary
- Background information
- Business objectives
- User needs and pain points
- Market/competitive landscape (if applicable)

#### Problem Statement
- Clear definition of the problem
- Impact of the problem on users/business
- Data supporting the problem existence

#### Solution Opportunity
- High-level overview of the proposed solution
- How it addresses the problem
- Expected outcomes and benefits

#### Functional Requirements
- List of high-level features and capabilities
- **For short PRD**: Focus on main features only
- **For full PRD**: Include detailed specifications:
  - User flows and interactions
  - System behaviors and rules
  - Integration points with other systems
  - Edge cases and error handling

### 2.1 Acceptance Criteria in PRDs

#### Macro-Level Acceptance Criteria (PRD)
- **Purpose**: Define the "what" not the "how"
- **Format**: High-level statements of functionality
- **Focus**: Business outcomes and user value
- **Examples**:
  - ✅ "User can filter search results by price range"
  - ✅ "System validates user email format during registration"
  - ❌ Avoid: "Show error message in red below the email field"

#### What to Avoid in PRD Acceptance Criteria
- Implementation details
- UI/UX specifics (belong in design documents)
- Technical specifications
- Micro-interactions (save for user stories)

#### When to Create Detailed Acceptance Criteria
- During story creation (not in PRD)
- When breaking down features into development tasks
- When working with UX/design teams on specific flows

### 3. PRD-Specific Validation

In addition to the standard validation, ensure PRD acceptance criteria:
1. **Remain at the right level**:
   - Focus on business requirements, not implementation
   - Avoid UI/UX details (these belong in design documents)
   - Don't specify technical solutions

2. **Are testable but not prescriptive**:
   - Should be verifiable
   - Should not dictate how to implement
   - Should allow for multiple implementation approaches
1. Review against the Product Documentation Constitution:
   - Is every requirement clear and unambiguous? (Principle I)
   - Are acceptance criteria based on designs? (Principle II)
   - Does it focus on functionality rather than description? (Principle III)
   - Is the level of detail appropriate for a PRD? (Principle IV)
   - Have all assumptions been validated? (Principle V)
2. Get user feedback
3. Update the PRD based on feedback
4. Add version history

## PRD-Specific Best Practices
### General PRD Guidelines
- Keep it concise but complete
- Use visual aids (diagrams, mockups) when helpful
- Link to supporting documents rather than duplicating content
- Maintain a single source of truth
- Update the PRD as requirements evolve

## Template
Use the PRD template located at: `templates/prd-template.md`

## Next Steps
After PRD approval, consider:
1. Creating a roadmap plan using the `plan` workflow
2. Breaking down requirements into user stories with `create-stories`

## Common Pitfalls to Avoid
- Writing requirements that are too detailed (save for stories)
- Not including success metrics
- Failing to validate assumptions
- Not updating the PRD when requirements change
- Creating requirements without user input
