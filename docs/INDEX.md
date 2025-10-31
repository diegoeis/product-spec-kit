# Documentation Index - Product Spec Kit v2.0

Quick reference to all documentation.

---

## 🚀 Getting Started

| Document | Description | When to Read |
|----------|-------------|--------------|
| [README.md](../README.md) | Overview and features | First stop - understand what this skill does |
| [QUICKSTART.md](QUICKSTART.md) | 5-minute guide | Ready to start immediately |
| [INSTALL.md](INSTALL.md) | Installation instructions | Before using the skill |
| [STRUCTURE.md](STRUCTURE.md) | File organization | Understanding how files are organized |

---

## 📚 Core Documentation

### Principles & Guidelines

| Document | Description |
|----------|-------------|
| [constitution.md](../memory/constitution.md) | 5 non-negotiable principles for all documentation |

### Templates

| Template | Purpose | Workflow |
|----------|---------|----------|
| [prd-template.md](../templates/prd-template.md) | Product Requirements Document | create-prd |
| [plan-template.md](../templates/plan-template.md) | Release & Execution Plan | create-plan |
| [stories-template.md](../templates/stories-template.md) | User Stories Collection | create-stories |
| [quick-issue-template.md](../templates/quick-issue-template.md) | Quick Issues (Stories, Bugs, Tasks, Spikes) | quick-* |
| [checklist-template.md](../templates/checklist-template.md) | Quality Validation Checklist | All workflows |

---

## 🎯 Workflows

### Full Documentation Workflows

| Workflow | Command Example | Documentation |
|----------|----------------|---------------|
| **create-prd** | "Create PRD for push notifications" | See [WORKFLOWS.md](WORKFLOWS.md#create-prd) |
| **clarify-prd** | "Clarify my PRD" | See [WORKFLOWS.md](WORKFLOWS.md#clarify-prd) |
| **create-plan** | "Create plan from my PRD" | See [WORKFLOWS.md](WORKFLOWS.md#create-plan) |
| **create-stories** | "Generate stories for first epic" | See [WORKFLOWS.md](WORKFLOWS.md#create-stories) |
| **clarify-stories** | "Clarify my stories" | See [WORKFLOWS.md](WORKFLOWS.md#clarify-stories) |
| **analyze** | "Analyze my documentation" | See [WORKFLOWS.md](WORKFLOWS.md#analyze) |

### Quick Issue Workflows

| Workflow | Command Example | Documentation |
|----------|----------------|---------------|
| **quick-story** | "Quick story: export to PDF" | See [WORKFLOWS.md](WORKFLOWS.md#quick-story) |
| **quick-bug** | "Document bug: login fails" | See [WORKFLOWS.md](WORKFLOWS.md#quick-bug) |
| **quick-task** | "Task: migrate database" | See [WORKFLOWS.md](WORKFLOWS.md#quick-task) |
| **quick-spike** | "Spike: research auth providers" | See [WORKFLOWS.md](WORKFLOWS.md#quick-spike) |

---

## 🌍 Language Support

| Language | Auto-Detection | Override Command |
|----------|----------------|------------------|
| English | ✅ Yes | "Respond in English" |
| Portuguese | ✅ Yes | "Responda em português" |
| Spanish | ✅ Yes | "Responde en español" |

---

## 📋 Reference Materials

### Quick References

| Topic | Location |
|-------|----------|
| **5 Constitution Principles** | [constitution.md](../memory/constitution.md#core-principles) |
| **When to Use What** | [README.md](../README.md#-when-to-use-what) |
| **Export Formats** | [README.md](../README.md#-export-formats) |
| **Troubleshooting** | [README.md](../README.md#-troubleshooting) |
| **Quality Checklist** | [checklist-template.md](../templates/checklist-template.md) |

### Examples

| Example Type | Location |
|--------------|----------|
| **PRD Example** | [examples/prd-example.md](../examples/prd-example.md) |
| **Full Workflow Example** | [QUICKSTART.md](QUICKSTART.md#your-first-prd) |
| **Quick Issue Example** | [QUICKSTART.md](QUICKSTART.md#your-first-quick-story) |

---

## 🔧 Technical Reference

### File Structure

```
product-spec-kit/
├── SKILL.md              # Main skill definition
├── README.md             # Overview & quick start
├── CHANGELOG.md          # Version history
├── templates/            # Document templates
├── memory/              # Core principles
├── examples/            # Sample documents
└── docs/                # Documentation
    ├── QUICKSTART.md    # 5-minute guide
    ├── INSTALL.md       # Installation
    ├── WORKFLOWS.md     # Detailed workflows
    ├── INDEX.md         # This file
    └── STRUCTURE.md     # File organization
```

Full details: [STRUCTURE.md](STRUCTURE.md)

---

## 📊 Version Information

| Version | Release Date | Key Changes |
|---------|--------------|-------------|
| v2.0.0 | 2025-10-30 | Multi-language, quick issues, export formats |
| v1.0.0 | 2025-10-29 | Initial release |

Full changelog: [CHANGELOG.md](../CHANGELOG.md)

---

## 🎯 Common Tasks

### I Want To...

| Task | Start Here |
|------|-----------|
| **Learn what this skill does** | [README.md](../README.md) |
| **Install the skill** | [INSTALL.md](INSTALL.md) |
| **Get started quickly** | [QUICKSTART.md](QUICKSTART.md) |
| **Create my first PRD** | [WORKFLOWS.md](WORKFLOWS.md#create-prd) |
| **Create a quick story** | [WORKFLOWS.md](WORKFLOWS.md#quick-story) |
| **Document a bug** | [WORKFLOWS.md](WORKFLOWS.md#quick-bug) |
| **Understand the principles** | [constitution.md](../memory/constitution.md) |
| **See examples** | [examples/](../examples/) |
| **Troubleshoot issues** | [INSTALL.md](INSTALL.md#common-installation-issues) |
| **Check version history** | [CHANGELOG.md](../CHANGELOG.md) |
| **Understand file structure** | [STRUCTURE.md](STRUCTURE.md) |

---

## 🆘 Help & Support

### Troubleshooting

1. **Installation issues**: [INSTALL.md](INSTALL.md#common-installation-issues)
2. **Workflow issues**: [README.md](../README.md#-troubleshooting)
3. **Quality issues**: [checklist-template.md](../templates/checklist-template.md)

### Best Practices

- **Always start with**: [constitution.md](../memory/constitution.md)
- **When in doubt**: Use [QUICKSTART.md](QUICKSTART.md)
- **For detailed guidance**: See [WORKFLOWS.md](WORKFLOWS.md)

---

## 📱 Quick Commands Cheat Sheet

```
# Language
"Respond in English" / "Responda em português"

# Full Workflows
"Create PRD for [feature]"
"Clarify my PRD"
"Create plan from PRD"
"Generate stories for [epic]"
"Analyze my documentation"

# Quick Issues
"Quick story: [description]"
"Document bug: [problem]"
"Task: [work]"
"Spike: [question]"

# Export
"Export in Jira format"
"Export for Linear"
"Show as GitHub issue"
```

---

## 🎓 Learning Path

### Beginner (Day 1)

1. Read [README.md](../README.md)
2. Follow [QUICKSTART.md](QUICKSTART.md)
3. Create your first quick story
4. Review [constitution.md](../memory/constitution.md)

### Intermediate (Week 1)

1. Create full PRD using [create-prd workflow](WORKFLOWS.md#create-prd)
2. Generate plan and stories
3. Use clarify workflows
4. Check [examples/](../examples/)

### Advanced (Month 1)

1. Master all 10 workflows
2. Customize for your team
3. Integrate with your tools
4. Contribute improvements

---

## 📞 Feedback

Found an issue? Have a suggestion? 

- Check [CHANGELOG.md](../CHANGELOG.md) for planned features
- Review [constitution.md](../memory/constitution.md) for principles
- See [README.md](../README.md) for contact info

---

**Last Updated**: 2025-10-30  
**Version**: 2.0.0  
**Skill Name**: Product Spec Kit
