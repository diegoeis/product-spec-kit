---
description: non-negotiable principles to maintain patterns and govern all documentations created with this skill
---

# Product Documentation Constitution

These are the **non-negotiable principles** that govern all product documentation created with this skill. These principles apply regardless of language, workflow type (full or quick), or document format.

---

## Core Principles

### I. User Value First

**Principle**: Every piece of work must clearly articulate value to end users.

**What This Means**:
- Every requirement in a PRD must explain how it helps users
- Every epic in a Plan must state user benefit
- Every user story must follow "As a [user], I want [capability], so that [benefit]"
- Even technical tasks must explain indirect user value

**Why It Matters**:
Without clear user value, teams build features nobody needs. This principle keeps everyone focused on outcomes, not outputs.

**Validation Questions**:
- Who benefits from this?
- What problem does this solve for them?
- How will their life/work be better?
- Would users pay for this?

**Examples**:

✅ **Good**:
- "As a customer support agent, I want to see customer purchase history, so that I can resolve issues faster without asking repetitive questions."
- "Migrate to PostgreSQL 15 to enable faster query performance, reducing dashboard load times from 5s to <1s, improving analyst productivity."

❌ **Bad**:
- "As a user, I want a button"
- "Implement caching" (no user value explained)
- "Refactor authentication module" (technical work without user impact)

**Application to Workflows**:
- **PRDs**: Every requirement must state user value
- **Plans**: Every epic must articulate user benefit
- **Stories**: Must use proper user story format with "so that" benefit clause
- **Quick Stories**: Same requirement as full stories
- **Technical Tasks**: Must explain how this enables/improves user experience
- **Bugs**: Impact on users must be documented
- **Spikes**: Must connect research to user-facing decision

---

### II. Testable Criteria

**Principle**: All success criteria and acceptance criteria must be objective and verifiable.

**What This Means**:
- Use concrete, measurable language
- Avoid subjective terms: "intuitive", "easy", "fast", "simple"
- Use specific metrics: "<200ms response time", "95% of users complete flow", "5/5 CSAT score"
- Acceptance criteria must have clear pass/fail states
- Use GIVEN-WHEN-THEN format for clarity

**Why It Matters**:
Vague criteria lead to endless debates about "done". Testable criteria create shared understanding and enable objective validation.

**Validation Questions**:
- How will we know if this is working?
- What specific metric will we measure?
- Can a QA engineer test this without ambiguity?
- Would two people agree on whether this is met?

**Examples**:

✅ **Good**:
- "Response time < 200ms for 95th percentile"
- "GIVEN user is on checkout page WHEN they click 'Pay' THEN payment processes and confirmation appears within 3 seconds"
- "95% of users complete onboarding flow in < 5 minutes"
- "Zero crashes reported in production for 30 days"

❌ **Bad**:
- "System should be fast"
- "UI should be intuitive"
- "Users should easily find features"
- "Performance should be good"
- "Should work well on mobile"

**Application to Workflows**:
- **PRDs**: Success metrics must be specific and measurable
- **Plans**: Each epic must have quantifiable success criteria
- **Stories**: Acceptance criteria must be objective, use GIVEN-WHEN-THEN
- **Quick Stories**: Same standard as full stories
- **Technical Tasks**: Define concrete deliverables and success criteria
- **Bugs**: Expected behavior must be specific
- **Spikes**: Define what specific question will be answered

---

### III. Complete Context

**Principle**: Each document must be understandable on its own, without requiring tribal knowledge.

**What This Means**:
- Include all necessary background
- Define abbreviations and jargon on first use
- Link to related documents
- Explain "why" decisions were made
- Document assumptions
- Don't assume everyone was in the meeting

**Why It Matters**:
People join teams, context gets lost, memories fade. Self-contained documents ensure everyone can contribute regardless of when they joined.

**Validation Questions**:
- Could a new team member understand this?
- Are all abbreviations defined?
- Is the "why" explained?
- Are related docs linked?
- Would this make sense in 6 months?

**Examples**:

✅ **Good**:
- "We're building email notifications because 73% of users reported missing important updates (see user research doc). This feature will address the #1 user complaint from Q3 surveys."
- "API (Application Programming Interface) latency must be < 200ms because our SLA (Service Level Agreement) commits to sub-second response times."

❌ **Bad**:
- "Per the meeting, we're doing notifications"
- "Because Bob said so"
- "Everyone knows why this is important"
- References to discussions without links or summaries
- Unexplained technical decisions

**Application to Workflows**:
- **PRDs**: Include problem context, why now, related initiatives
- **Plans**: Reference PRD, explain phasing decisions
- **Stories**: Include background, fit in epic context
- **Quick Stories**: Provide enough context to execute without asking questions
- **Quick Bugs**: Document environment, steps, expected behavior
- **Quick Tasks**: Explain why this work matters
- **Quick Spikes**: Clarify what decision depends on this research

---

### IV. Prioritized Work

**Principle**: Every piece of work must have a clear priority and realistic effort estimate.

**What This Means**:
- Use consistent priority framework (Critical/High/Medium/Low or P0/P1/P2)
- Priority should reflect business/user impact
- Estimates should be relative and realistic
- Dependencies must be explicit
- Work should be sequenced logically

**Why It Matters**:
Without priorities, teams thrash. With priorities, teams execute efficiently and deliver maximum value.

**Validation Questions**:
- What happens if we don't do this?
- What gets blocked if this isn't done?
- How does this compare to other work?
- Is the estimate realistic given team capacity?
- What are the dependencies?

**Examples**:

✅ **Good**:
- "P0 (Critical): Payment processing broken - revenue impact, affects all users"
- "P1 (High): Mobile responsive layout - 40% of users on mobile, workaround exists"
- "P2 (Medium): Dark mode - requested by 15% of users, no business impact"
- "Estimate: M (3-5 days) based on similar work last quarter"

❌ **Bad**:
- "Everything is P0"
- "This is important" (relative to what?)
- "Should be quick" (how quick?)
- No estimate provided
- Estimate: "As fast as possible"

**Application to Workflows**:
- **PRDs**: Requirements must be P0/P1/P2
- **Plans**: Epics must be sequenced with rationale
- **Stories**: Priority + estimate required
- **Quick Stories**: Priority + estimate required
- **Quick Bugs**: Severity + Priority + estimate for fix
- **Quick Tasks**: Priority with business justification
- **Quick Spikes**: Time-box mandatory (2-8 hours typical, max 2 days)

---

### V. Consistent Terminology

**Principle**: Use the same terms for the same concepts across all documentation.

**What This Means**:
- Pick one term and stick with it
- Create a glossary for key concepts
- Don't use synonyms for core entities
- Align terminology across PRD → Plan → Stories
- Use industry-standard terms when applicable

**Why It Matters**:
Inconsistent terminology creates confusion. "Customer" vs "User" vs "Client" - are these the same? Different? Nobody knows, so everyone wastes time clarifying.

**Validation Questions**:
- Are we using the same term we used in the PRD?
- Do we have multiple terms for the same thing?
- Would a new team member be confused?
- Is there a glossary if terms are complex?

**Examples**:

✅ **Good**:
- **Consistent**: Always use "workspace" (not sometimes "space", "area", "room")
- **Glossary**: "Workspace: a collaborative area where team members share documents"
- **Standard Terms**: Use industry terms like "API", "SaaS", "MRR"

❌ **Bad**:
- **Inconsistent**: "workspace" in PRD, "space" in Plan, "room" in stories
- **Made-up Terms**: "doohickey" instead of standard "widget"
- **Undefined Jargon**: Using company-specific abbreviations without definition

**Application to Workflows**:
- **PRDs**: Define key terms in glossary
- **Plans**: Use exact terms from PRD
- **Stories**: Match terminology from PRD and Plan
- **Quick Issues**: Use established terminology or define new terms

---

## Principle Application by Workflow

### Full Workflow (PRD → Plan → Stories)

All five principles apply strictly:
1. ✅ User value in every requirement, epic, story
2. ✅ Testable metrics and acceptance criteria
3. ✅ Complete context in each document
4. ✅ Clear priorities and sequencing
5. ✅ Consistent terminology across all docs

### Quick Issues Workflow

All five principles still apply, adapted for single-item creation:

**Quick Stories**:
- ✅ User value in story format
- ✅ Testable acceptance criteria (GIVEN-WHEN-THEN)
- ✅ Sufficient context to execute (may need to request more)
- ✅ Priority and estimate
- ✅ Consistent with existing terminology

**Quick Bugs**:
- ✅ User impact documented
- ✅ Reproducible steps (testable)
- ✅ Complete environment and context
- ✅ Severity and priority
- ✅ Consistent terminology

**Quick Tasks**:
- ✅ User/business value explained (even if indirect)
- ✅ Success criteria testable
- ✅ Complete technical context
- ✅ Priority with justification
- ✅ Standard technical terms

**Quick Spikes**:
- ✅ User/business value of decision to be made
- ✅ Testable: clear question to answer, deliverable defined
- ✅ Complete context for research
- ✅ Time-boxed (priority by urgency)
- ✅ Consistent terminology

---

## Enforcement

### How Principles Are Enforced

**During Creation**:
- Skill actively checks for principle violations
- Missing elements trigger questions to user
- Templates include principle reminders

**During Review**:
- Checklist includes constitution validation
- Analyze workflow cross-checks principles
- Non-compliance is flagged before finalization

**Error Messages**:

If principle violated, skill responds:

**Principle I (User Value)**:
```
⚠️ Constitution Violation: User Value First

This [story/requirement/epic] doesn't clearly articulate user value.

Current: "[current text]"

Required: Explain WHO benefits and HOW their life/work improves.

Question: How will users benefit from this specifically?
```

**Principle II (Testable Criteria)**:
```
⚠️ Constitution Violation: Testable Criteria

This acceptance criterion uses vague language: "[vague term]"

Vague terms like "fast", "easy", "intuitive" are not testable.

Required: Use specific, measurable criteria.

Example:
❌ "System should be fast"
✅ "API response time < 200ms for 95th percentile"

Can you provide a specific, measurable criterion?
```

**Principle III (Complete Context)**:
```
⚠️ Constitution Violation: Complete Context

This document references "[undefined term/abbreviation]" without definition.

Required: Define all abbreviations and provide context.

Question: Can you explain what "[term]" means?
```

**Principle IV (Prioritized Work)**:
```
⚠️ Constitution Violation: Prioritized Work

This [item] is missing [priority/estimate].

Required: All work must have priority and realistic estimate.

Question: What's the priority and estimated effort?
```

**Principle V (Consistent Terminology)**:
```
⚠️ Constitution Violation: Consistent Terminology

You're using "[term1]" here but used "[term2]" in [previous doc].

Are these the same concept?

Required: Use consistent terminology across all documents.

Question: Which term should we use consistently?
```

---

## Exceptions

### When Principles Can Be Relaxed

**NEVER**: Principles I (User Value) and II (Testable Criteria) cannot be waived.

**RARELY**: Principles III, IV, V can be temporarily relaxed only when:
- User explicitly requests quick draft
- Document is marked "DRAFT - INCOMPLETE"
- Clear plan exists to complete before finalization

**NEVER SHIP**: Documentation violating principles should not be used for:
- Stakeholder reviews
- Development sprint planning
- Team execution
- External communication

---

## Summary

**The Five Non-Negotiable Principles**:

1. 🎯 **User Value First**: Every piece of work must clearly benefit users
2. ✅ **Testable Criteria**: All success/acceptance criteria must be objective and measurable
3. 📚 **Complete Context**: Documents must be self-contained and understandable
4. 🎚️ **Prioritized Work**: Every item must have priority and realistic estimate
5. 📖 **Consistent Terminology**: Same terms for same concepts across all docs

**Apply to everything**: PRDs, Plans, Stories, Quick Issues, all workflows, all languages.

**Non-negotiable**: These principles cannot be waived for "speed" or "convenience".

**Quality over quantity**: Better to create fewer documents that follow principles than many that don't.
