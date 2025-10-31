# Quick Start Guide - Product Spec Kit v2.0

Get started in 5 minutes! 🚀

## Installation

```bash
# 1. Copy skill to Claude
cp -r product-spec-kit ~/.config/claude/skills/user/

# 2. Restart Claude Desktop

# 3. Verify
Open new chat and say: "Do I have Product Spec Kit installed?"
```

## Your First Quick Story

**Step 1**: Open Claude and say:
```
"Quick story: users want to export their reports to PDF format"
```

**Step 2**: Claude asks for context:
```
To make this better, can you share:
- What reports specifically?
- Any existing export functionality?
- Business priority for this?
```

**Step 3**: You provide context:
```
Monthly sales reports. We currently only have CSV export. 
This is high priority - top customer request.
```

**Step 4**: Claude creates complete story:
```markdown
STORY-2025-10-30-001: Export Monthly Reports to PDF

Priority: High
Estimate: M (3-5 days)

As a sales manager
I want to export monthly sales reports to PDF format
So that I can share professional-looking reports with stakeholders

[Complete acceptance criteria, edge cases, etc.]
```

**Step 5**: Choose export format:
```
"Export this in Jira format"
```

Done! ✅

---

## Your First PRD

**Step 1**: Say:
```
"I want to create a PRD for a push notification system"
```

**Step 2**: Claude asks questions:
```
Great! Let me ask a few questions:
1. Who are the primary users?
2. What's the main business goal?
3. Are there any technical constraints?
```

**Step 3**: You answer, Claude creates PRD

**Step 4**: Download or save to repository

**Step 5**: Continue with:
```
"Create a plan from my PRD"
→ "Generate stories for the first epic"
```

---

## Quick Commands Reference

### Quick Issues
```
"Quick story: [description]"
"Document bug: [problem]"
"Task: [technical work]"
"Spike: [research question]"
```

### Full Workflows
```
"Create PRD for [feature]"
"Clarify my PRD"
"Create plan from PRD"
"Generate stories for [epic]"
"Analyze my documentation"
```

### Language
```
"Responda em português"
"Respond in English"
"Responde en español"
```

---

## Common Scenarios

### Scenario 1: Bug Found in Production
```
You: "Document bug: users can't login after password reset"

Claude: [asks for reproduction steps, impact]

You: [provides details]

Claude: [creates structured bug report with severity]
```

### Scenario 2: Technical Debt
```
You: "Task: migrate database to PostgreSQL 15"

Claude: Can you explain the user/business value?

You: This will improve dashboard load times from 5s to <1s

Claude: [creates task with clear value proposition]
```

### Scenario 3: Need to Research
```
You: "Spike: research best caching solution for our API"

Claude: [creates time-boxed investigation with clear deliverables]
```

---

## Pro Tips

1. **More Context = Better Quality**
   - Share PRDs, docs, background
   - Explain the "why"
   - Mention related features

2. **Use Clarify Workflows**
   - "Clarify my PRD" - gets better questions
   - "Clarify this story" - improves acceptance criteria

3. **Check Constitution**
   - All docs must have user value
   - Acceptance criteria must be testable
   - Priority required

4. **Right-size Your Approach**
   - Major feature? Full PRD
   - Bug or small change? Quick issue
   - Not sure? Start with quick issue

5. **Iterate**
   - Create draft
   - Review
   - Clarify
   - Finalize

---

## Troubleshooting

**"Skill not found"**
→ Check installation path, restart Claude

**"Language wrong"**
→ Say: "respond in [your language]"

**"Context not enough"**
→ Share more background, docs, examples

**"Story too vague"**
→ Use "clarify" workflow

---

## Next Steps

- Read [README.md](../README.md) for complete overview
- Check [WORKFLOWS.md](WORKFLOWS.md) for detailed guides
- Review [constitution.md](../memory/constitution.md) for principles
- See [examples](../examples/) for inspiration

---

## Need Help?

- Check [README Troubleshooting](../README.md#-troubleshooting)
- Review [constitution principles](../memory/constitution.md)
- Look at [templates](../templates/) for format examples

**Happy documenting!** 🎉
