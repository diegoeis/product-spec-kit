---
date_modified: 2025-10-31
---

# Product Spec Kit 🚀

A comprehensive framework for creating and managing product documentation with AI assistance. Perfect for both new projects and existing products, helping teams maintain high-quality specifications from concept to implementation.

This focus on product specification phase, usually made by Product Managers and Designers. We will focus in the upstream track, to give more power to PMs, Designers and other people that need to create specifications to use with AI or for common process.

## ✨ Why Use This Kit?

- **AI-Powered Documentation**: Leverage AI to create, refine, and maintain your product specifications
- **Structured Workflows**: Clear processes for every stage of product development
- **Time-Saving Templates**: Ready-to-use templates for all your documentation needs
- **Consistent Quality**: Built-in validation ensures high standards across all documents
- **Seamless Integration**: Works with your existing tools and workflows

## 🚀 Quick Start

### For New Projects
1. Start with a PRD using `create-prd`
2. Generate a release plan with `plan`
3. Break down into epics and stories
4. Keep documentation in sync as you build

### For Existing Projects
1. Document current state with quick issues
2. Fill documentation gaps systematically
3. Standardize your existing specs
4. Improve consistency across teams

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

## 📚 Core Workflows

### Full Product Lifecycle
1. **PRD Creation**: `create-prd`
2. **Release Planning**: `plan`
3. **Epic Definition**: `create-epic`
4. **Story Writing**: `create-issue`

### Quick Documentation
- `quick-story`: Single user story
- `quick-bug`: Bug report
- `quick-task`: Technical task
- `quick-spike`: Research task

## 🛠️ Key Features

### For Product Teams
- Clear documentation hierarchy
- AI-assisted requirement gathering
- Consistent formatting and structure
- Built-in best practices

### For Developers
- Clear acceptance criteria
- Technical considerations
- Integration points
- Testable requirements

## 📋 Constitution Principles

All documentation follows these non-negotiable principles:

1. **User Value First**: Every piece of work must clearly benefit users
2. **Testable Criteria**: All acceptance criteria must be objective
3. **Complete Context**: Documents must be self-contained
4. **Prioritized Work**: Every item needs priority and estimate
5. **Consistent Terminology**: Same terms across all docs

## 🌟 Getting the Most from AI

1. **Be Specific**: Provide clear context about your project
2. **Use Visuals**: Share mockups or diagrams when available
3. **Iterate**: Use `clarify` to refine outputs
4. **Validate**: Cross-check AI suggestions with your domain knowledge

## 📂 Project Structure

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

## 🎨 Export & Integration

### Export Formats
- **Markdown**: Universal format
- **Jira**: Ready to paste
- **Linear**: Native format
- **GitHub Issues**: With labels
- **Azure DevOps**: Work items

### AI Integration
- Works with major LLM providers
- Supports context-aware completions
- Maintains conversation history

## 💡 When to Use What

| Scenario | Recommended Workflow |
|----------|---------------------|
| New major feature | Full workflow (PRD → Plan → Epics → Stories) |
| Existing product audit | Start with quick issues, then structure |
| Bug found | Quick bug |
| Small improvement | Quick story |
| Technical debt | Quick task |
| Research needed | Quick spike |
| Documentation update | Quick task with PRD reference |

## 🤝 Contributing

We welcome contributions! Please see our [Contribution Guidelines](CONTRIBUTING.md) for details.

---

*Built with ❤️ for product teams who believe in the power of great documentation.*
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
- [product-speckit-constitution.md](prompts/my-skills/product-spec-kit/rules/product-speckit-constitution.md) - Core principles

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

And so many thanks for [spec-kit](https://github.com/github/spec-kit) people. This project was inspired by their work.


## 📄 License

Open source - use freely for your product documentation needs.

