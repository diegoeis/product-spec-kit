---
date_modified: 2025-10-30
---
# README

Complete framework for Product Managers and Designers to create high-quality product documentation with AI assistance.

## 🚀 Quick Start

### For Full Documentation
```
"I want to create a PRD for push notifications"
→ Skill creates complete PRD
→ "Create a plan from my PRD"
→ Skill generates release plan
→ "Generate stories for first epic"
→ Skill creates detailed user stories
```

### For Quick Issues
```
"Quick story: users want to export reports to PDF"
→ Skill creates standalone story

"Document bug: login fails after password reset"
→ Skill creates structured bug report

"Task: migrate database to PostgreSQL 15"
→ Skill creates technical task

"Spike: research authentication providers"
→ Skill creates time-boxed investigation
```

## 📚 Workflows

### Full Workflows
1. **create-prd**: Product Requirements Document
2. **clarify-prd**: Refine PRD with targeted questions
3. **create-plan**: Release plan with epics and stories
4. **create-stories**: Detailed user stories
5. **clarify-stories**: Refine stories
6. **analyze**: Cross-document consistency check

### Quick Issue Workflows (NEW)
7. **quick-story**: Standalone user story
8. **quick-bug**: Bug report
9. **quick-task**: Technical task
10. **quick-spike**: Research/investigation

## 📋 Constitution Principles

All documentation follows 5 non-negotiable principles:

1. **User Value First**: Every piece of work must clearly benefit users
2. **Testable Criteria**: All acceptance criteria must be objective
3. **Complete Context**: Documents must be self-contained
4. **Prioritized Work**: Every item needs priority and estimate
5. **Consistent Terminology**: Same terms across all docs

## 📂 Structure

```
product-spec-kit/
├── SKILL.md              # Main skill file
├── README.md             # This file
├── templates/
│   ├── prd-template.md
│   ├── plan-template.md
│   ├── stories-template.md
│   ├── quick-issue-template.md  (NEW)
│   └── checklist-template.md
├── memory/
│   └── constitution.md   # Non-negotiable principles
├── examples/
│   └── prd-example.md
└── docs/
    ├── QUICKSTART.md
    ├── INSTALL.md
    └── WORKFLOWS.md
```

## 🎨 Export Formats

Quick issues can export to:
- **Markdown**: Universal format
- **Jira**: Ready to paste
- **Linear**: Native format
- **GitHub Issues**: With labels
- **Azure DevOps**: Work items

## 💡 When to Use What

| Scenario | Use This |
|----------|----------|
| New major feature | Full workflow (PRD → Plan → Stories) |
| Bug found | Quick bug |
| Small improvement | Quick story |
| Technical debt | Quick task |
| Research needed | Quick spike |
| Regular sprint work | Full workflow or quick stories |

## ✅ Quality Assurance

Before finalizing any document:
- [ ] All 5 constitution principles met
- [ ] Acceptance criteria are testable
- [ ] Context is complete
- [ ] Priority assigned
- [ ] Terminology consistent

## 📖 Documentation

- [QUICKSTART.md](docs/QUICKSTART.md) - 5-minute guide
- [INSTALL.md](docs/INSTALL.md) - Installation instructions
- [WORKFLOWS.md](docs/WORKFLOWS.md) - Detailed workflow guide
- [constitution.md](memory/constitution.md) - Core principles

## 🔧 Installation

```bash
# Copy to Claude skills directory
cp -r product-spec-kit ~/.config/claude/skills/user/

# Restart Claude Desktop

# Verify installation
"Do I have Product Spec Kit installed?"
```

See [INSTALL.md](docs/INSTALL.md) for detailed instructions.

## 🆘 Troubleshooting

**Language detected wrong?**
→ Say: "respond in [your language]"

**Quick issue lacks context?**
→ Provide PRD, docs, or more background

**Stories too large?**
→ Use clarify-stories workflow

**Can't write to repository?**
→ Use download option instead

## 📝 Examples

### Example 1: Full Workflow
User creates PRD → Plan → Stories for complete feature documentation

### Example 2: Quick Story
User needs single story for small feature, provides context, gets ready-to-use story

### Example 3: Bug Report
User describes bug, skill structures it with reproduction steps and impact

See [examples/](examples/) for complete examples.

## 🎯 Tips for Success

1. **Start with Why**: Always clarify the user problem
2. **Iterate**: Use clarify workflows
3. **Right-size**: Not everything needs full PRD
4. **Context Matters**: More context = better outputs
5. **Review Constitution**: When in doubt, check principles

## 📊 Version History

- **v2.0** (2025-10-30): Multi-language, quick issues, export formats
- **v1.0** (2025-10-29): Initial release

## 🤝 Contributing

This skill evolves based on user needs. Feedback welcome!

## 📄 License

Open source - use freely for your product documentation needs.

---

**Ready to get started?** Check out [QUICKSTART.md](docs/QUICKSTART.md)!
