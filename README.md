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

## What tools to use this kit?

Use this kit with any tool thats supports Projects or in Claude Skills. 

Originally created for Claude, but can be used with any tool that supports Projects, just creating a new project in your tool and copying the content of this repository to the your LLM Project.


I try to make it as simple as possible to be portable, following folder and file structure used by IDEs, like Windsurf and Cursor, maintaing the possibility to be used in Projects or Claude Skills. But, my recommendation is to use it with Claude Skills.

When using in Projects, copy/paste the description below in the Project instructions. You can ignore that if you are using Claude Skills.

```
You will help managers and product teams to create and maintain high-quality product specifications. You will use the all the guidelines and instructions, step by step described in the SKILL.md located in the project base knowledge.

Some descriptions will refer to files using relative paths, like `templates/prd-template.md` or `workflows/create-prd.md`. You can find the content of these files in the project base knowledge, ignore the file path.

Read the SKILL.md file to get priority information before you do anything else. The SKILL.md file is your priority guide and need to be read before you do anything else. SKILL.md centralizes all instructions and rules for the Product Spec Kit.
```

## 🚀 Quick Start

Using Claude Skills or Projects, you can start using this kit using some key words to trigger the skill or to be specific when you are using in LLM Projects scope.

*Some examples:*

- "I want to *create a PRD* for push notifications, using following informations to create it and guide me through the process."
- "Create a *plan* from my PRD"
- "Help me *clarify* my PRD"

## 📚 Core Workflows

### Full Product Lifecycle
1. **PRD Creation**: `create-prd`
2. **Release Planning**: `plan`
3. **Epic Definition**: `create-epic`
4. **Story Writing**: `create-issue`

---

*Built with ❤️ for product teams who believe in the power of great documentation to potentialize value for business and users.*

## Contributing

This skill evolves based on user needs. Feedback welcome!

And so many thanks for [spec-kit](https://github.com/github/spec-kit) people. This project was inspired by their work.


## 📄 License

Open source - use freely for your product documentation needs.

