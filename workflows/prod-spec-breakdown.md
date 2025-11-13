---
description: Workflow for creating a product release plan using the plan template.
auto_execution_mode: 1
---

# Breakdown Specs Workflow

This workflow guides you through creating a structured product release plan using the `templates/prod-breakdown-template.md`. This plan is used to break down a large initiative into manageable chunks, providing a high-level roadmap for product development.

## When to Use
- After PRD approval and before development begins
- When you need to break down a large initiative into manageable chunks
- When you need to break down a large epic into stories / tasks
- To align stakeholders on release strategy and timing
- When you need to sequence work across multiple teams

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
- Suggest the creation of this section in next steps after finalizing the breakdown
- Technical or cross-team dependencies
- Potential risks and mitigation strategies
- Resource requirements and constraints

## Steps to Create a breakdown

### 1. Initial Setup
1. Create a new markdown file using `templates/prod-breakdown-template.md`
2. Use the naming convention: `{initiative-name}-breakdown-plan.md`
3. Fill in the document metadata

### 2. Define Releases
1. Break down the product roadmap into logical releases
2. For each release:
   - Define the goal and objectives
   - Identify key epics
   - Set high-level timeline expectations
3. Define the dates for releases, epics and stories based in throughput, velocity or leadtime provided by the user. If user provide those data, calculate based on it. If not, asks to user to provide the date ranges.
4. Asks to user to confirm the relationship between releases, epics and stories.

### 3. Break Down Epics
1. For each epic:
   - Define the problem it solves
   - List high-level acceptance criteria
   - Identify related stories (can be placeholders)
   - Note any technical considerations
   - The goals need to be clear and achievable based on user journey and behavior, not the tech details.

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
Use the plan template located at: `templates/prod-breakdown-template.md`

## Integration with Other Workflows
- **PRD**: This plan should align with the approved PRD
- **Epics**: Use `templates/prod-epic-template.md` for detailed epic documentation
- **Stories**: Use `templates/prod-story-template.md` for detailed story writing
- **Tasks**: Use `templates/prod-story-template.md` for detailed task writing

## Next Steps After Creating this breakdown
1. Build epic files with detailed stories
2. Refine based on feedback
3. Create the Dependency Matrix section
4. Create the Risk Management section