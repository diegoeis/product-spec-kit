---
date_modified: 2025-10-30
---
# Changelog

All notable changes to Product Spec Kit will be documented in this file.

## [1.0.0] - 2025-10-30

### 🎉 Initial Release

#### Multi-Language Support
- **Auto-Detection**: Skill automatically detects user's language from first message
- **Supported Languages**: English, Portuguese (Português), Spanish (Español)
- **Manual Override**: Users can specify language explicitly
- **Template Adaptation**: All templates and responses adapt to detected language

#### Quick Issue Workflows
- **quick-story**: Create standalone user stories without full PRD/Plan
- **quick-bug**: Structure bug reports with reproduction steps and impact
- **quick-task**: Document technical tasks with business value
- **quick-spike**: Create time-boxed research/investigation tasks

#### Enhanced Context Management
- Skill now requests additional context when creating quick issues
- Prompts for PRDs, documents, artifacts to improve quality
- Smart context inference based on available information

#### Export Formats
- **Jira**: Ready-to-paste format
- **Linear**: Native format support
- **GitHub Issues**: Markdown with labels
- **Azure DevOps**: Work item format
- **Markdown**: Universal format

### 📝 Documentation Improvements
- Complete rewrite of SKILL.md with all new workflows
- Added quick-issue-template.md with 4 issue types
- Updated constitution.md to cover quick issues
- Enhanced README.md with v2.0 features
- Added multi-language examples throughout

### 🔧 Template Updates
- **prd-template.md**: Translated to English, added multi-language headers
- **plan-template.md**: Translated to English, enhanced structure
- **stories-template.md**: Translated to English, improved acceptance criteria format
- **checklist-template.md**: Added quick issues validation section
- **quick-issue-template.md**: NEW - Complete templates for stories, bugs, tasks, spikes

### ✨ Constitution Changes
- Updated all 5 principles to explicitly cover quick issues
- Added enforcement guidelines for multi-language support
- Enhanced examples with Portuguese and Spanish versions
- Added error messages for principle violations

### 🐛 Bug Fixes
- Fixed path references from .specify/ to skill structure
- Removed bash script dependencies that don't work in LLMs
- Corrected workflow naming consistency

### 💡 Workflow Enhancements
- Added 4 new workflows (quick-story, quick-bug, quick-task, quick-spike)
- Enhanced existing 6 workflows with language detection
- Improved context gathering for all workflows
- Better validation against constitution principles

### 🎯 User Experience
- Clearer usage examples for each workflow
- Better error messages when principles violated
- Improved troubleshooting section
- More comprehensive examples

#### Core Workflows
- **create-prd**: Create Product Requirements Documents
- **clarify-prd**: Refine PRDs with targeted questions
- **plan**: Generate release plans with epics and stories
- **create-stories**: Create detailed user stories
- **clarify-stories**: Refine stories with questions
- **analyze**: Cross-document consistency validation

#### Constitution
- Established 5 core non-negotiable principles:
  1. User Value First
  2. Testable Criteria
  3. Complete Context
  4. Prioritized Work
  5. Consistent Terminology

#### Templates
- prd-template.md (PT-BR)
- plan-template.md (PT-BR)
- stories-template.md (PT-BR)
- checklist-template.md (PT-BR)

#### Documentation
- README.md
- SKILL.md
- constitution.md
- QUICKSTART.md
- INSTALL.md

#### Features
- Full PRD → Plan → Stories workflow
- Quality validation checklist
- Constitution principle enforcement
- Template-based document generation
- Download and repository integration options

---

## Version Numbering

We use [Semantic Versioning](https://semver.org/):
- **MAJOR** version for incompatible changes
- **MINOR** version for new functionality (backward compatible)
- **PATCH** version for bug fixes (backward compatible)

---

## Upgrade Guide

### From v1.0 to v2.0

**Breaking Changes**: None - v2.0 is fully backward compatible

**New Features**:
1. **Language Support**: Your documents will now be created in your language
2. **Quick Issues**: Use new workflows for faster documentation
3. **Export Formats**: Choose your project management tool format

**Migration Steps**:
1. Download v2.0 skill
2. Replace v1.0 in your skills directory
3. Restart Claude Desktop
4. Start using new workflows immediately

**Existing Documents**: All v1.0 documents remain valid and can be updated using v2.0 workflows

---

## Planned for v3.0

### Under Consideration
- Additional languages (French, German, Japanese)
- Integration with popular PM tools (direct API access)
- AI-powered suggestion engine for PRD improvements
- Template customization framework
- Collaborative editing features
- Version control integration

### Community Requests
Submit feature requests via feedback!

---

## Support

Having issues? Check:
1. [README.md](README.md) - Overview and quick start
2. [QUICKSTART.md](docs/QUICKSTART.md) - 5-minute guide
3. [WORKFLOWS.md](docs/WORKFLOWS.md) - Detailed workflow guide
4. [Troubleshooting](README.md#-troubleshooting) - Common issues

---

**Note**: Dates are in YYYY-MM-DD format (ISO 8601)
