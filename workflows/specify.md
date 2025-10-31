---
description: Workflow to generate epics and stories from a plan file.
auto_execution_mode: 1
---

# Specify Workflow

This workflow takes a plan file and generates the corresponding epics and user stories based on the plan's structure. It automates the creation of the entire specification hierarchy.

## When to Use
- After creating a plan and before starting development
- When you need to break down epics into detailed user stories
- To ensure consistency between your plan and implementation artifacts
- When onboarding new team members to understand the scope

## Prerequisites
- A completed plan file (created using `workflows/plan.md`)
- Associated PRD document (for context and requirements)
- Access to any relevant design documents or mockups
- Understanding of the product's technical constraints

## Input
- **Plan File**: Path to the plan file to process
- **PRD Context**: Reference to the related PRD (optional but recommended)
- **Output Directory**: Where to generate the specifications (default: `specs/[prd-name]/`)

## Process

### 1. Plan Analysis
1. Parse the plan file to extract:
   - Release structure
   - List of epics with descriptions
   - High-level stories/tasks
   - Dependencies and relationships
   - Acceptance criteria

### 2. Directory Structure Setup
```
specs/
└── [prd-name]/
    ├── [prd-name].md         # PRD document
    ├── [plan-name].md        # The source plan
    │
    ├── [epic-1]/             # Epic 1 directory
    │   ├── [epic-1].md       # Epic document
    │   ├── story-1.md        # User story 1
    │   └── story-2.md        # User story 2
    │
    └── [epic-2]/             # Epic 2 directory
        ├── [epic-2].md       # Epic document
        └── story-3.md        # User story 3
```

### 3. Epic Generation
For each epic in the plan:
1. Create a directory for the epic
2. Generate an epic markdown file using `templates/epic-template.md`
3. Include:
   - Epic name and description
   - Related PRD/plan references
   - High-level acceptance criteria
   - List of related stories
   - Technical considerations

### 4. Story Generation
For each story in an epic:
1. Create a story markdown file in the epic's directory
2. Use `templates/stories-template.md` as a base
3. Include:
   - User story format (As a... I want... So that...)
   - Detailed acceptance criteria
   - Design references
   - Technical notes
   - Dependencies

## Output
- **Epic Files**: One markdown file per epic in its own directory
- **Story Files**: One markdown file per story in its epic's directory
- **Index File**: (Optional) Summary of all generated artifacts
- **Report**: Summary of what was created and any issues found

## Error Handling
- If a required field is missing, prompt the user for input
- If a file already exists, skip or update based on user preference
- Log all actions for audit purposes

## Best Practices
1. **Review Before Committing**: Always review generated artifacts
2. **Version Control**: Add all new files to version control
3. **Link Artifacts**: Ensure all cross-references are properly linked
4. **Update Documentation**: Update any related documentation or trackers

## Implementation Notes

### Input Requirements
- A valid plan file following the plan template
- Related PRD document (recommended for context)
- Access to template files (epic-template.md, stories-template.md)

### Expected Behavior
1. Parse the plan file to understand the structure
2. Create the appropriate directory structure
3. Generate epic and story files based on templates
4. Preserve relationships between artifacts
5. Handle any missing information through user prompts

### Output Validation
- Verify all required files were created
- Check that all cross-references are valid
- Ensure consistent naming conventions
- Validate against template requirements

## Next Steps
1. Review generated epics and stories
2. Add any missing details or acceptance criteria
3. Share with the development team
4. Use as input for sprint planning
