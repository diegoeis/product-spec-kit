---
description: Quick start guide for the Product Spec Kit
auto_execution_mode: 1
---

# 🚀 Getting Started with Product Spec Kit

Welcome to the Product Spec Kit! This guide will help you quickly get started with creating and managing your product documentation.

Check the SKILL.md like your priority guide.

## 📋 Quick Reference

### Core Workflows
1. **Create a PRD**
   - Start with `create-prd` to define your product requirements
   - Uses: `templates/prd-template.md`

2. **Plan Your Release**
   - After PRD, use `plan` to create a release plan
   - Uses: `templates/plan-template.md`

3. **Define Epics**
   - Break down your plan into epics with `create-epic`
   - Uses: `templates/epic-template.md`

4. **Create Stories & Tasks**
   - Generate detailed user stories and tasks with `create-issue`
   - Uses: `templates/stories-template.md`

5. **Specify Implementation**
   - Convert your plan into detailed specs with `specify`
   - Works with your existing PRD and plan

### Quick Actions
- `quick-story`: Create a standalone user story
- `quick-bug`: Document a bug report
- `quick-task`: Create a technical task
- `quick-spike`: Document a research spike

## 📂 File Structure

All generated documents follow this structure:

```
specs/
└── [product-name]/
    ├── [product-name].md     # PRD
    ├── [plan-name].md        # Release Plan
    ├── [epic-1]/            # Epic directory
    │   ├── [epic-1].md      # Epic document
    │   ├── story-*.md       # User stories
    │   └── task-*.md        # Technical tasks
    └── [standalone-issue].md # Issues not in an epic
```

## 🛠️ Need Help?

- Run `clarify` on any document to improve its quality
- Check `SKILL.md` for detailed documentation
- Review the `templates/` directory for guidance on structure

## 🔄 Workflow

1. Start with a PRD or use an existing one
2. Create a release plan
3. Break down into epics
4. Generate detailed stories and tasks
5. Refine with your team

## 📝 Tips
- Use kebab-case for all filenames and directories
- Keep PRDs and plans in the root of your project
- Store all generated specs in the `specs/` directory
- Review all generated content before committing
