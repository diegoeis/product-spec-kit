---
name: [Name from PRD]  
team: [Team Name]
created_at: [YYYY-MM-DD]
last_updated: [YYYY-MM-DD]  
---

## Breakdown Plan Summary

{3-4 sentences: What we're building, Why we are building, how we will solve this  and expected impact}

---

## Deliverables Relationship

```
Release 1 {Date Range when provided. If not, ignore this field}
  ├── Epic 1.1 {Date when provided. If not, ignore this field}
  │   ├── Story/Task 1.1.1
  │   └── Story/Task 1.1.2
  └── Epic 1.2 {Date when provided. If not, ignore this field}
      ├── Story/Task 1.2.1
      └── Story/Task 1.2.2

Release 2 {Date Range when provided. If not, ignore this field}
  ├── Epic 2.1 {Date when provided. If not, ignore this field}
  │   └── Story/Task 2.1.1
  └── Epic 2.2 {Date when provided. If not, ignore this field}
      └── Story/Task 2.2.1
```

{after create this relationship, asks to validate if the relationship is correct. This is important to avoid errors in the breakdown plan.}

---

## Releases

### Release 1: {Name}

**Goal**: {What this release achieves. Point of view of the user, no tech details.}  
**Epics, stories and tasks included in this release**:
- {Epic name 1.1}
   - {Story 1.1.1}
   - {Story 1.1.2}
- {Epic name 1.2}
   - {Story 1.2.1}
   - {Story 1.2.2}

**Dependencies**:
- {write a list of dependencies based on design product and tech gaps identified or not given by the user}

**Risks and concerns**:
- {write a list of risks based on design product and tech gaps identified or not given by the user}

---

#### Epic 1.1: {Name}

**Outcome delivered**: {What this delivery accomplishes}

**User expectations**: {As a user, what value does this epic deliver?}

**Stories that deliver this epic**:
1. {Story 1.1.1 title}
2. {Story 1.1.2 title}
3. {Story 1.1.3 title}

**Acceptance Criteria (Epic-level)**:
- [ ] {List of high-level criteria. This criteria are used to validate the epic and create detailed stories}

**Work days**: {sum of work business days based on velocity or leadtime - if provided. If not, ignore this field}

---

##### Epic 1.1.2: {Epic Name}

{Same structure as Epic 1.1.1}

---

### Release 2: {Name}

{Same structure as Release 1}

---

## Dependencies & Sequencing

### Critical Path

```
Epic 1.1.1
   ↓
Epic 1.1.2 ──→ Epic 1.2.1
                   ↓
                Epic 2.1.1
```

### Dependency Matrix
{if asks to create the dependency matrix, create it. If not, ignore this section}

| Epic | Depends On | Blocks | Status |
|------|------------|--------|--------|
| Epic 1.1.1 | - | Epic 1.1.2 | Not Started |
| Epic 1.1.2 | Epic 1.1.1 | Epic 1.2.1 | Not Started |
| Epic 1.2.1 | Epic 1.1.2 | Epic 2.1.1 | Not Started |

### External Dependencies
{if asks to create the external dependencies, create it. If not, ignore this section}

- **{Dependency 1}**: {Description}
- **{Dependency 2}**: {Description}

---

## Risk Management
{if asks to create the risk management, create it. If not, ignore this section}

### High-Level Risks

| Risk | Impact | Likelihood | Mitigation | Owner | Status |
|------|--------|------------|------------|-------|--------|
| [Risk 1] | H/M/L | H/M/L | [Strategy] | [Name] | [Status] |
| [Risk 2] | H/M/L | H/M/L | [Strategy] | [Name] | [Status] |

### Contingency Plans

**If [Risk 1] occurs**:
1. [Action 1]
2. [Action 2]
3. [Fallback option]

**If [Risk 2] occurs**:
1. [Action 1]
2. [Action 2]
3. [Fallback option]
