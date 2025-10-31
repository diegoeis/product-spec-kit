# plan-template

This template provides structure to create a summary of a plan, detailing the structure of Releases, Epics and Issues.

---
**name**: [Name from PRD]  
**team**: [Team Name]
**created_at**: [YYYY-MM-DD]
**last_updated**: [YYYY-MM-DD]  
---

## Executive Summary

[3-4 sentences: What we're building, Why we are building, how we will solve this  and expected impact]

---

## Deliverables Relationship

```
Release 1 [Date Range - if provided]
  ├── Epic 1.1 [Date - if provided]
  │   ├── Story/Task 1.1.1
  │   └── Story/Task 1.1.2
  └── Epic 1.2 [Date - if provided]
      ├── Story/Task 1.2.1
      └── Story/Task 1.2.2

Release 2 [Date Range - if provided]
  ├── Epic 2.1 [Date - if provided]
  │   └── Story/Task 2.1.1
  └── Epic 2.2 [Date - if provided]
      └── Story/Task 2.2.1
```

---

## Releases

### Release 1: [Name]

**Goal**: [What this release achieves]  
**What includes this release**:
- [Epic name 1]
- [Epic name 2]

**Dependencies**:
- [Dependency 1]
- [Dependency 2]

**Risks**:
- **[Risk 1]**: [Mitigation]
- **[Risk 2]**: [Mitigation]

---

#### Epic 1.1: [Name]

**Focus**: [What this delivery accomplishes]

**User Value**: [As a user, what value does this epic deliver?]

**Story Outline**:
1. [Story 1 title]
2. [Story 2 title]
3. [Story 3 title]

**Acceptance Criteria (Epic-level)**:
- [ ] [High-level criterion 1]
- [ ] [High-level criterion 2]

**Target Date**: [Date - if provided]  
**Priority**: [High/Medium/Low]

---

##### Epic 1.1.2: [Epic Name]

[Same structure as Epic 1.1.1]

---

### Release 2: [Name]

[Same structure as Release 1]

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

| Epic | Depends On | Blocks | Status |
|------|------------|--------|--------|
| Epic 1.1.1 | - | Epic 1.1.2 | Not Started |
| Epic 1.1.2 | Epic 1.1.1 | Epic 1.2.1 | Not Started |
| Epic 1.2.1 | Epic 1.1.2 | Epic 2.1.1 | Not Started |

### External Dependencies

- **[Dependency 1]**: [Description] - Owner: [Name] - ETA: [Date]
- **[Dependency 2]**: [Description] - Owner: [Name] - ETA: [Date]

---

## Resource Planning

### Team Allocation

| Team/Squad | Release 1 | Release 2 | Notes |
|------------|-----------|-----------|-------|
| [Team 1] | [%] | [%] | [Context] |
| [Team 2] | [%] | [%] | [Context] |

### Key People

| Role | Name | Responsibility | Availability |
|------|------|----------------|--------------|
| Product Manager | [Name] | [Scope] | [%] |
| Engineering Lead | [Name] | [Scope] | [%] |
| Design Lead | [Name] | [Scope] | [%] |
| QA Lead | [Name] | [Scope] | [%] |

---

## Success Metrics & KPIs

### Leading Indicators (During Development)

| Metric | Target | Current | Status |
|--------|--------|---------|--------|
| Sprint velocity | [X] | [Y] | 🟢/🟡/🔴 |
| Story completion rate | [X%] | [Y%] | 🟢/🟡/🔴 |
| Bug backlog | [X] | [Y] | 🟢/🟡/🔴 |

### Lagging Indicators (After Launch)

| Metric | Baseline | Target | Measurement Date | Actual |
|--------|----------|--------|------------------|--------|
| [Metric 1] | [X] | [Y] | [Date] | [Z] |
| [Metric 2] | [X] | [Y] | [Date] | [Z] |

---

## Risk Management

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

---

## Communication Plan

### Status Updates

- **Frequency**: [Weekly/Bi-weekly]
- **Format**: [Email/Slack/Meeting]
- **Audience**: [Who]
- **Owner**: [Who sends updates]

### Stakeholder Reviews

| Milestone | Date | Audience | Format |
|-----------|------|----------|--------|
| [Review 1] | [Date] | [Who] | [Demo/Presentation] |
| [Review 2] | [Date] | [Who] | [Demo/Presentation] |

### Launch Communication

- **Internal Announcement**: [Date] - [Channel]
- **External Announcement**: [Date] - [Channel]
- **Documentation**: [Date] - [Where]

---

## Quality Assurance

### Testing Strategy

**Unit Testing**:
- [Coverage target]
- [Responsibility]

**Integration Testing**:
- [Scope]
- [Timeline]

**User Acceptance Testing**:
- [Who]
- [When]
- [Criteria]

**Performance Testing**:
- [Metrics]
- [Targets]

### Definition of Done (Per Story)

- [ ] Code complete and reviewed
- [ ] Unit tests written and passing
- [ ] Integration tests passing
- [ ] Documentation updated
- [ ] Design review approved
- [ ] Product owner accepted
- [ ] Deployed to staging
- [ ] QA signed off

---

## Launch Readiness

### Pre-Launch Checklist

**Technical**:
- [ ] All P0 stories complete
- [ ] Performance targets met
- [ ] Security review passed
- [ ] Load testing complete
- [ ] Rollback plan tested

**Documentation**:
- [ ] User documentation complete
- [ ] API documentation complete
- [ ] Support runbooks ready
- [ ] Training materials ready

**Operations**:
- [ ] Monitoring in place
- [ ] Alerts configured
- [ ] Support team trained
- [ ] Incident response plan ready

**Go-to-Market**:
- [ ] Marketing assets ready
- [ ] Communication plan approved
- [ ] Sales/CS briefed
- [ ] Legal/compliance approved

---

## Post-Launch

### Monitoring Plan

**Week 1**:
- Daily metric reviews
- Daily bug triage
- Daily stakeholder updates

**Week 2-4**:
- [Frequency] metric reviews
- [Frequency] retrospective
- Success criteria evaluation

### Success Evaluation

**Date**: [30/60/90 days post-launch]  
**Evaluation Criteria**:
- [ ] Success metrics achieved
- [ ] User feedback positive
- [ ] No critical issues
- [ ] Team velocity maintained

### Retrospective

**Date**: [Date]  
**Participants**: [Who]  
**Focus**:
- What went well
- What could improve
- Action items for next release

---

## Appendix

### Glossary

- **[Term 1]**: [Definition]
- **[Term 2]**: [Definition]

### Related Documents

- [Link to PRD]
- [Link to technical design]
- [Link to user research]
- [Link to competitive analysis]

### Version History

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| 1.0 | [Date] | Initial plan | [Name] |
| 1.1 | [Date] | [Changes] | [Name] |

---

## Constitution Validation

- [ ] ✅ **User Value First**: Every epic has clear user benefit
- [ ] ✅ **Testable Criteria**: Success metrics are measurable
- [ ] ✅ **Complete Context**: Plan is self-contained
- [ ] ✅ **Prioritized Work**: Clear sequencing and priorities
- [ ] ✅ **Consistent Terminology**: Aligned with PRD terminology
