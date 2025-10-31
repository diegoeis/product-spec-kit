# File Structure - Product Spec Kit v2.0

Detailed explanation of the skill's file organization.

---

## Directory Tree

```
product-spec-kit/
├── SKILL.md                          # Main skill definition file
├── README.md                         # Overview, quick start, features
├── CHANGELOG.md                      # Version history and updates
│
├── templates/                        # Document templates
│   ├── prd-template.md              # PRD structure (full & short formats)
│   ├── plan-template.md             # Release plan structure
│   ├── stories-template.md          # User stories collection format
│   ├── quick-issue-template.md      # Quick issues (stories/bugs/tasks/spikes)
│   └── checklist-template.md        # Quality validation checklist
│
├── references/                           # Core principles and rules
│   └── constitution.md              # 5 non-negotiable principles
│   └── clarify.md              # Questions to clarify PRD/Story/Tasks
│
├── examples/                         # Sample documents
│   └── prd-example.md               # Complete PRD example
│
└── docs/                            # Documentation
    ├── QUICKSTART.md                # 5-minute getting started guide
    ├── INSTALL.md                   # Installation instructions
    ├── WORKFLOWS.md                 # Detailed workflow documentation
    ├── INDEX.md                     # Documentation index
    └── STRUCTURE.md                 # This file
```

---

## File Descriptions

### Root Level Files

#### SKILL.md
**Purpose**: Main skill definition file that Claude reads  
**Contains**:
- Skill description and capabilities
- Language detection rules
- All 10 workflow definitions (6 full + 4 quick)
- Usage examples
- Constitution validation rules
- Troubleshooting guide

**Used by**: Claude Desktop when loading the skill

---

#### README.md
**Purpose**: Human-readable overview and quick reference  
**Contains**:
- What's new
- Quick start examples
- Workflow summary
- Language support info
- When to use what guide
- Export formats
- Troubleshooting

**Used by**: Users learning about the skill

---

#### CHANGELOG.md
**Purpose**: Version history and release notes  
**Contains**:
- Version-by-version changes
- Feature additions
- Bug fixes
- Breaking changes
- Upgrade guides
- Planned features

**Used by**: Users tracking versions and updates

---

### templates/ Directory

Contains all document structure templates that the skill uses to generate documentation.

#### prd-template.md
**Purpose**: Product Requirements Document template  
**Contains**:
- Executive summary structure
- Problem statement format
- Goals & metrics section
- User personas template
- Requirements breakdown (P0/P1/P2)
- Technical considerations
- Go-to-market sections
- **Two formats**: Full (comprehensive) and Short (lightweight)
- Multi-language headers (EN/PT/ES)

**Used by**: `create-prd` workflow

---

#### plan-template.md
**Purpose**: Release and execution plan template  
**Contains**:
- Roadmap visualization
- Release strategy
- Deliveries and epics structure
- Story outlines
- Dependency mapping
- Resource planning
- Risk management
- Success metrics

**Used by**: `create-plan` workflow

---

#### stories-template.md
**Purpose**: User stories collection template  
**Contains**:
- User story format (As a... I want... So that...)
- Acceptance criteria (GIVEN-WHEN-THEN)
- Edge cases and error handling
- Technical notes
- Dependencies
- Testing notes
- Definition of done

**Used by**: `create-stories` workflow

---

#### quick-issue-template.md (NEW in v2.0)
**Purpose**: Quick standalone issues template  
**Contains**:
- **User Story template**: For quick stories
- **Bug template**: Reproduction steps, impact
- **Technical Task template**: With business value
- **Spike template**: Time-boxed research
- Naming conventions
- Priority guidelines
- Estimation guidelines
- Export formats (Jira/Linear/GitHub/Azure)

**Used by**: `quick-story`, `quick-bug`, `quick-task`, `quick-spike` workflows

---

#### checklist-template.md
**Purpose**: Quality validation checklist  
**Contains**:
- PRD quality checks
- Plan quality checks
- Stories quality checks
- Quick issues quality checks
- Cross-document consistency checks
- Language & communication checks
- Pre-sharing checklist

**Used by**: All workflows for validation, `analyze` workflow

---

### references/ Directory

Contains core principles and rules that govern all documentation.

#### constitution.md
**Purpose**: Non-negotiable principles for all documentation  
**Contains**:
- **5 Core Principles**:
  1. User Value First
  2. Testable Criteria
  3. Complete Context
  4. Prioritized Work
  5. Consistent Terminology
- Principle explanations with examples
- Application to each workflow
- Enforcement rules
- Error messages
- Language-agnostic application

**Used by**: All workflows for validation and quality enforcement

---

### examples/ Directory

Contains sample documents showing best practices.

#### prd-example.md
**Purpose**: Complete example of a well-written PRD  
**Contains**:
- Real-world PRD for a push notification system
- Demonstrates all principles
- Shows good vs bad examples
- Illustrates proper formatting

**Used by**: Users learning to write good PRDs

**Note**: More examples can be added (plan examples, story examples, etc.)

---

### docs/ Directory

Contains all user-facing documentation.

#### QUICKSTART.md
**Purpose**: 5-minute getting started guide  
**Contains**:
- Installation steps
- First quick story walkthrough
- First PRD walkthrough
- Quick commands reference
- Common scenarios
- Pro tips
- Troubleshooting basics

**Used by**: New users getting started

---

#### INSTALL.md
**Purpose**: Detailed installation instructions  
**Contains**:
- Platform-specific installation (macOS/Windows/Linux)
- Verification steps
- Common installation issues
- MCP configuration (optional)
- Updating from v1.0 to v2.0
- Uninstallation
- Multi-user installation

**Used by**: Users installing or troubleshooting installation

---

#### WORKFLOWS.md
**Purpose**: Detailed documentation for all workflows  
**Contains**: (Will be created)
- Step-by-step guide for each workflow
- When to use each workflow
- Detailed examples
- Best practices
- Common pitfalls
- Tips and tricks

**Used by**: Users working with specific workflows

---

#### INDEX.md
**Purpose**: Master index of all documentation  
**Contains**:
- Quick reference table
- Links to all documents
- Common tasks guide
- Quick commands cheat sheet
- Learning path
- Help resources

**Used by**: Users finding specific information

---

#### STRUCTURE.md
**Purpose**: This file - explains file organization  
**Contains**:
- Directory tree
- File descriptions
- Purpose of each file
- How files relate to each other
- What each file is used for

**Used by**: Users understanding the skill's structure

---

## File Relationships

### Workflow → Files Used

| Workflow | Files Used |
|----------|-----------|
| **create-prd** | SKILL.md, prd-template.md, constitution.md, checklist-template.md |
| **clarify-prd** | SKILL.md, constitution.md |
| **create-plan** | SKILL.md, plan-template.md, constitution.md, checklist-template.md |
| **create-stories** | SKILL.md, stories-template.md, constitution.md, checklist-template.md |
| **clarify-stories** | SKILL.md, constitution.md |
| **analyze** | SKILL.md, constitution.md, checklist-template.md |
| **quick-story** | SKILL.md, quick-issue-template.md, constitution.md |
| **quick-bug** | SKILL.md, quick-issue-template.md, constitution.md |
| **quick-task** | SKILL.md, quick-issue-template.md, constitution.md |
| **quick-spike** | SKILL.md, quick-issue-template.md, constitution.md |

---

## File Dependencies

```
SKILL.md (core)
├── Reads: constitution.md (principles)
├── Uses: prd-template.md (for PRDs)
├── Uses: plan-template.md (for plans)
├── Uses: stories-template.md (for stories)
├── Uses: quick-issue-template.md (for quick issues)
└── Validates with: checklist-template.md

constitution.md (principles)
└── Applied by: All workflows

Templates (all)
├── Follow: constitution.md principles
└── Validated by: checklist-template.md

Documentation (all)
├── Reference: All templates
├── Explain: constitution.md
└── Guide: SKILL.md workflows
```

---

## File Sizes (Approximate)

| File | Size | Lines | Notes |
|------|------|-------|-------|
| SKILL.md | ~15 KB | ~300 | Main skill definition |
| README.md | ~6 KB | ~200 | Overview |
| CHANGELOG.md | ~6 KB | ~180 | Version history |
| constitution.md | ~14 KB | ~450 | Core principles |
| prd-template.md | ~9 KB | ~280 | PRD structure |
| plan-template.md | ~9 KB | ~300 | Plan structure |
| stories-template.md | ~5 KB | ~150 | Stories format |
| quick-issue-template.md | ~14 KB | ~450 | Quick issues |
| checklist-template.md | ~6 KB | ~200 | Quality checks |
| QUICKSTART.md | ~4 KB | ~150 | Quick start |
| INSTALL.md | ~8 KB | ~280 | Installation |
| INDEX.md | ~6 KB | ~200 | Documentation index |
| STRUCTURE.md | ~7 KB | ~250 | This file |

**Total**: ~100 KB (compressed to ~37 KB in ZIP)

---

## Modification Guidelines

### When to Modify Each File

**SKILL.md**:
- Adding new workflows
- Changing workflow behavior
- Updating language detection
- Modifying validation rules

**Templates**:
- Changing document structure
- Adding new sections
- Updating format conventions
- Adding new issue types

**constitution.md**:
- Updating core principles (rare!)
- Adding principle examples
- Clarifying enforcement rules

**Documentation**:
- Adding examples
- Improving explanations
- Fixing errors
- Adding new guides

---

## Version Control Best Practices

### Critical Files (Test Before Changing)
- SKILL.md
- constitution.md
- All templates

### Documentation Files (Safer to Change)
- README.md
- All docs/ files
- CHANGELOG.md

### Always Update After Changes
- CHANGELOG.md (document changes)
- Version numbers in:
  - README.md
  - SKILL.md
  - CHANGELOG.md
  - INDEX.md

---

## Installation Directory Structure

When installed, the skill appears at:

**macOS/Linux**:
```
~/.config/claude/skills/user/product-spec-kit/
└── [all files and directories as shown above]
```

**Windows**:
```
%APPDATA%\Claude\skills\user\product-spec-kit\
└── [all files and directories as shown above]
```

---

## Future Additions

Planned files for future versions:

- `examples/plan-example.md` - Example release plan
- `examples/stories-example.md` - Example user stories
- `docs/WORKFLOWS.md` - Detailed workflow guide
- `docs/API.md` - Programmatic usage (if applicable)
- `templates/custom-template.md` - User customization guide

---

**Last Updated**: 2025-10-30  
**Version**: 2.0.0
