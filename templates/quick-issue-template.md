# Quick Issue Templates

This file contains templates for creating standalone issues without full PRD/Plan context.

## Template Selection Guide

| Issue Type | When to Use | Key Elements |
|------------|-------------|--------------|
| **User Story** | Feature request, user need | User value, acceptance criteria |
| **Bug** | Defect, broken functionality | Reproduction steps, impact |
| **Technical Task** | Infrastructure, refactoring | Technical work, business value |
| **Spike** | Research, investigation | Question, time-box, deliverable |

---

## User Story Template

```markdown
# [STORY-YYYY-MM-DD-###]: [Action-Oriented Title]

**Type**: User Story  
**Priority**: [Critical/High/Medium/Low]  
**Estimate**: [XS/S/M/L/XL]  
**Status**: Backlog  

## User Story

**As a** [type of user]  
**I want** [capability]  
**So that** [benefit/value]

## Context

[Background information, related features, business goals]

## Acceptance Criteria

- [ ] **GIVEN** [initial context]  
      **WHEN** [action taken]  
      **THEN** [expected outcome]

- [ ] **GIVEN** [another context]  
      **WHEN** [action taken]  
      **THEN** [expected outcome]

- [ ] [Additional criterion if needed]

## Edge Cases

- **[Edge case 1]**: [How to handle]
- **[Edge case 2]**: [How to handle]

## Out of Scope

- [What this story explicitly does NOT include]
- [Deferred items]

## Dependencies

- [ ] [Dependency 1 - with status]
- [ ] [Dependency 2 - with status]

## Technical Notes

[Any implementation guidance, constraints, or considerations]

## Design Assets

- [Link to mockups/wireframes if available]
- [Link to design specs if available]

## Success Metrics

- [How we'll measure if this delivers value]
- [Expected impact]

## Labels

`user-story`, `[priority-label]`, `[area/team]`, `[feature-group]`

---

## Constitution Validation

- [ ] ✅ Clear user value stated (Principle I)
- [ ] ✅ Testable acceptance criteria (Principle II)
- [ ] ✅ Sufficient context provided (Principle III)
- [ ] ✅ Priority indicated (Principle IV)
- [ ] ✅ Consistent terminology (Principle V)
```

---

## Bug Template

```markdown
# [BUG-YYYY-MM-DD-###]: [Problem Statement]

**Type**: Bug  
**Severity**: [Critical/High/Medium/Low]  
**Priority**: [Critical/High/Medium/Low]  
**Status**: To Do  
**Environment**: [Production/Staging/Development]

## Summary

[Clear, concise description of the problem]

## Impact

**Users Affected**: [All users / Specific segment / % affected]  
**Business Impact**: [Revenue/UX/Reputation impact]  
**Workaround Available**: [Yes/No - describe if yes]

## Steps to Reproduce

1. [First step]
2. [Second step]
3. [Third step]
4. [Result]

## Expected Behavior

[What should happen]

## Actual Behavior

[What actually happens]

## Screenshots/Videos

[Attach visual evidence]

## Environment Details

- **Browser/App**: [Browser version or app version]
- **OS**: [Operating system and version]
- **Device**: [Device type if relevant]
- **User Role**: [User permissions/role if relevant]
- **Date/Time**: [When bug occurred]

## Console Errors

```
[Paste any console errors or logs]
```

## Reproduction Rate

[Always / Sometimes (X%) / Rare] - [Context when it happens]

## Root Cause (if known)

[Technical explanation if already identified]

## Proposed Solution

[How to fix, if idea exists]

## Related Issues

- [Link to related bugs/stories]
- [Similar past issues]

## Labels

`bug`, `[severity]`, `[area/component]`, `[browser/platform]`

---

## Constitution Validation

- [ ] ✅ Reproducible steps provided (Principle II)
- [ ] ✅ Complete context included (Principle III)
- [ ] ✅ Priority/severity clear (Principle IV)
- [ ] ✅ Consistent terminology (Principle V)
```

---

## Technical Task Template

```markdown
# [TASK-YYYY-MM-DD-###]: [Work Description]

**Type**: Technical Task  
**Priority**: [Critical/High/Medium/Low]  
**Estimate**: [Hours or Days]  
**Status**: Backlog  

## Task Description

[Clear description of the technical work to be done]

## Business/User Value

**Why this matters**: [Explain impact even if indirect]
- [How this helps users]
- [How this helps business]
- [How this enables future work]

## Deliverables

- [ ] [Specific deliverable 1]
- [ ] [Specific deliverable 2]
- [ ] [Documentation updated]
- [ ] [Tests written]

## Success Criteria

- [ ] [Measurable criterion 1]
- [ ] [Measurable criterion 2]
- [ ] [Performance/quality target]

## Technical Details

### Current State
[What exists now]

### Desired State
[What we want to achieve]

### Approach
[How we'll do it - high level]

## Dependencies

- [ ] [Dependency 1]
- [ ] [Dependency 2]

## Risks

- **[Risk 1]**: [Mitigation strategy]
- **[Risk 2]**: [Mitigation strategy]

## Testing Strategy

[How to verify this works]

## Rollback Plan

[How to revert if needed]

## Documentation Needs

- [ ] [Update technical docs]
- [ ] [Update runbooks]
- [ ] [Update architecture diagrams]

## Labels

`technical-task`, `[priority]`, `[area/system]`, `[type-of-work]`

---

## Constitution Validation

- [ ] ✅ Clear user/business value explained (Principle I)
- [ ] ✅ Testable success criteria (Principle II)
- [ ] ✅ Complete technical context (Principle III)
- [ ] ✅ Priority indicated (Principle IV)
- [ ] ✅ Consistent terminology (Principle V)
```

---

## Spike Template

```markdown
# [SPIKE-YYYY-MM-DD-###]: [Question to Answer]

**Type**: Spike (Research/Investigation)  
**Time-box**: [2-8 hours typical, max 2 days]  
**Priority**: [High/Medium/Low]  
**Status**: To Do  

## Question to Answer

[Clear, specific question that needs answering]

## Context

[Why we need this answered, what decision depends on it]

## Success Criteria

This spike is successful when we can:
- [ ] [Decision criterion 1]
- [ ] [Decision criterion 2]
- [ ] Make informed decision on [what]

## Investigation Areas

- [ ] [Area 1 to research]
- [ ] [Area 2 to research]
- [ ] [Area 3 to research]

## Evaluation Criteria

| Criterion | Weight | Notes |
|-----------|--------|-------|
| [Performance] | [High/Med/Low] | [What matters] |
| [Cost] | [High/Med/Low] | [Budget constraints] |
| [Complexity] | [High/Med/Low] | [Team capability] |
| [Maintenance] | [High/Med/Low] | [Long-term impact] |

## Expected Deliverables

- [ ] **Findings Document**: Summary of research
- [ ] **Options Comparison**: Pros/cons of each approach
- [ ] **Recommendation**: Specific suggestion with rationale
- [ ] **Next Steps**: Clear actions based on findings

## Out of Scope

[What this spike explicitly does NOT investigate]

## Follow-up Actions

**If Option A**: [What tasks follow]  
**If Option B**: [What tasks follow]  
**If needs more research**: [Extended spike or different approach]

## Resources

- [Documentation links]
- [Similar implementations to study]
- [People to consult]

## Time-box Checkpoint

**After [X] hours**: Review findings, decide if continuing or concluding

## Labels

`spike`, `research`, `[area]`, `[technology]`

---

## Constitution Validation

- [ ] ✅ Clear question to answer (Principle II)
- [ ] ✅ Complete context for why (Principle III)
- [ ] ✅ Time-boxed (Principle IV)
- [ ] ✅ Actionable deliverable defined (Principle II)
```

---

## Naming Convention

### Format
`[TYPE]-[YYYY-MM-DD]-[###]`

### Components

- **TYPE**: STORY, BUG, TASK, SPIKE, EPIC
- **Date**: Creation date (YYYY-MM-DD)
- **Sequence**: 001, 002, 003... (increment daily)

### Examples

```
STORY-2025-10-30-001
BUG-2025-10-30-005
TASK-2025-10-30-002
SPIKE-2025-10-30-001
```

### Titles

- **User Story**: Action-oriented (e.g., "Add items to cart")
- **Bug**: Problem statement (e.g., "Login timeout after 30 seconds")
- **Task**: Work description (e.g., "Migrate database to PostgreSQL 15")
- **Spike**: Question format (e.g., "Research caching solutions for API")

---

## Priority Guidelines

### 🔴 Critical/High

- **Blocks** other work
- **Security** or data loss risk
- **Affects** many users
- **Business critical** impact

### 🟡 Medium

- **Important** but not blocking
- **Affects** some users
- **Has workaround**
- **Planned** work

### 🟢 Low

- **Nice to have**
- **Optimization**
- **Minimal** user impact
- **Can be deferred**

---

## Estimation Guidelines

### For Stories/Tasks

- **XS**: < 1 day
- **S**: 1-2 days
- **M**: 3-5 days
- **L**: 1-2 weeks
- **XL**: > 2 weeks (consider breaking down)

### For Bugs

- Estimate **fix time** in hours/days
- Include time for **testing and verification**

### For Spikes

- Always **time-box**
- Typical: **2-8 hours**
- Maximum: **2 days**

---

## Export Formats

### For Jira

```
**Summary:** [Title]
**Description:** [Full content from template]
**Issue Type:** [Story/Bug/Task]
**Priority:** [High/Medium/Low]
**Labels:** [labels]
**Story Points:** [estimate]
```

### For Linear

```
**Title:** [Title]
**Description:** [Full content]
**Status:** Backlog
**Priority:** [0-4 scale]
**Labels:** [labels]
**Estimate:** [points]
```

### For GitHub Issues

```markdown
### [Title]

[Full content from template]

**Labels:** `[type]`, `[priority]`, `[area]`
**Assignees:** @username
**Projects:** [project name]
```

### For Azure DevOps

```
**Title:** [Title]
**Work Item Type:** [User Story/Bug/Task]
**Description:** [Full content]
**Priority:** [1-4]
**Effort:** [estimate]
**Tags:** [labels]
```

---

## Usage Flow

### 1. User Initiates
```
"Create a story: users want to filter by date"
"Document bug: login fails after password reset"
"Task: implement Redis caching"
"Spike: research authentication providers"
```

### 2. Skill Detects Type & Language
- Identifies issue type (story/bug/task/spike)
- Detects user language
- Selects appropriate template

### 3. Context Gathering
**For Stories:**
- User persona
- Related features
- Business goals
- Existing docs/PRDs

**For Bugs:**
- Environment
- Steps to reproduce
- Expected vs actual behavior
- Impact assessment

**For Tasks:**
- Technical background
- Business/user value
- Dependencies
- Success criteria

**For Spikes:**
- Decision to be made
- Evaluation criteria
- Time-box
- Expected output

### 4. Template Population
- Fills template with gathered information
- Validates against constitution
- Ensures quality standards

### 5. Review & Export
- Presents formatted issue
- Offers export options
- Saves to files or repository

---

## Quality Checklist

Before finalizing any quick issue:

**All Issues:**
- [ ] Clear, descriptive title
- [ ] Type correctly identified
- [ ] Priority assigned
- [ ] Estimate provided
- [ ] Labels suggested
- [ ] Constitution principles met

**User Stories:**
- [ ] User value clear
- [ ] Acceptance criteria testable
- [ ] Edge cases considered
- [ ] Dependencies identified

**Bugs:**
- [ ] Reproducible steps
- [ ] Expected vs actual clear
- [ ] Impact assessed
- [ ] Environment documented

**Technical Tasks:**
- [ ] User/business value explained
- [ ] Success criteria defined
- [ ] Deliverables specific
- [ ] Testing strategy included

**Spikes:**
- [ ] Question specific
- [ ] Time-boxed
- [ ] Deliverables defined
- [ ] Follow-up actions clear

---

## Tips for Better Quick Issues

### Do's ✅

- **Provide context**: More info = better quality
- **Link related docs**: Reference PRDs, designs, existing features
- **Be specific**: Vague inputs → vague outputs
- **Use examples**: Show what good looks like
- **Think user first**: Even for technical work, explain user value

### Don'ts ❌

- **Don't skip context**: "Add filter" is too vague
- **Don't assume knowledge**: Explain abbreviations, jargon
- **Don't mix types**: One issue = one type
- **Don't ignore constitution**: Principles apply to all issues
- **Don't estimate blindly**: Consider complexity realistically

### Examples

**Bad**: "Add filter"  
**Good**: "Add date range filter to transactions list so users can analyze specific time periods"

**Bad**: "Fix login bug"  
**Good**: "Login times out after 30 seconds on mobile Safari, affecting ~15% of users"

**Bad**: "Update database"  
**Good**: "Migrate to PostgreSQL 15 to enable better performance for reporting queries (user benefit: faster dashboard loads)"

**Bad**: "Research options"  
**Good**: "Research caching solutions (Redis vs Memcached) to decide on architecture for reducing API response times to <200ms"

---

## Workflow Integration

Quick issues can coexist with full workflows:

```
PRD Created
  ↓
Plan Generated
  ↓
Stories Created ────────┐
  ↓                     │
[Development starts]    │
  ↓                     │
Quick Bug Created ←─────┤
Quick Story Added ←─────┤
Quick Task Logged ←─────┘
```

**When to use each:**

| Scenario | Approach |
|----------|----------|
| Major new feature | Full workflow (PRD → Plan → Stories) |
| Bug found in testing | Quick bug |
| User requests small change | Quick story |
| Technical debt identified | Quick task |
| Need to evaluate approach | Quick spike |
| Adding to existing feature | Quick story (reference PRD) |
| Refactoring | Quick task |
| Production incident | Quick bug (Critical priority) |

---

## Language Variations

Templates support multiple languages. Examples:

### Portuguese (Português)

```markdown
# [STORY-2025-10-30-001]: [Título Orientado à Ação]

**Tipo**: História de Usuário  
**Prioridade**: [Crítica/Alta/Média/Baixa]  
**Estimativa**: [XS/S/M/L/XL]  

## História de Usuário

**Como** [tipo de usuário]  
**Eu quero** [capacidade]  
**Para que** [benefício/valor]

## Contexto
[...]
```

### Spanish (Español)

```markdown
# [STORY-2025-10-30-001]: [Título Orientado a la Acción]

**Tipo**: Historia de Usuario  
**Prioridad**: [Crítica/Alta/Media/Baja]  
**Estimativa**: [XS/S/M/L/XL]  

## Historia de Usuario

**Como** [tipo de usuario]  
**Quiero** [capacidad]  
**Para** [beneficio/valor]

## Contexto
[...]
```

Language is detected automatically and templates adapt accordingly.
