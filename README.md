---
date_modified: 2025-10-31
---

# Product Spec Kit 🚀

A comprehensive framework for creating and managing product documentation with AI assistance. Perfect for both new projects and existing products, helping teams maintain high-quality specifications from concept to implementation.

Focused on the specification phase, this kit empowers Product Managers and Designers to create clear, actionable specs for AI applications and standard processes.

Compatible with any LLM platform supporting Projects or Claude Skills, with a file structure that follows standard IDE conventions for easy integration.

## ✨ Why Use This Kit?

- **AI-Powered Documentation**: Leverage AI to create, refine, and maintain your product specifications
- **Structured Workflows**: Clear processes for every stage of product development
- **Time-Saving Templates**: Ready-to-use templates for all your documentation needs
- **Consistent Quality**: Built-in validation ensures high standards across all documents
- **Seamless Integration**: Works with your existing tools and workflows

## Installation

1. Download this repository. 
2. For Claude Skills: [follow the official instructions](https://support.claude.com/en/articles/12512180-using-skills-in-claude).

For other LLM platforms
1. unzip the repository;
2. Open your preferred LLM and create a new project;
3. Copy the following files to the new LLM project:
    - `SKILL.md` file
    - Copy all markdown files from the `workflows`, `rules`, `templates`, and `example` of respository folders
    - Add the following instructions to your project configuration:

```
You will help managers and product teams to create and maintain high-quality product specifications. You will use the all the guidelines and instructions, step by step described in the SKILL.md located in the project base knowledge.

Some descriptions may reference files using relative paths (e.g., `templates/prd-template.md` or `workflows/create-prd.md`). The content of these files is available in the project's base knowledge; you can safely ignore the file paths.

Before proceeding, carefully review the SKILL.md file. This is your primary reference that centralizes all instructions and rules for the Product Spec Kit. Reading this file first is essential for proper implementation.
```

## Quick Start

After installation, you can start using the Product Spec Kit by using the following prompts. If you are using Claude Skills, try:

```
I want to create a PRD using Product Spec Kit instructions, with following informations:

We will build a simple to-do list product called *Awesome Todo List*. Build the PRD following this informations:

- The want to benefit users who have problems with an effective organization using tasks to direct the main objectives of their day and week.
- We want to create a simple frictionless product, without bureaucracy, so people can organize themselves without large bureaucracies. 
- The flow is simple: The user enters the page, add to-dos, without having to login or signup.

- Some functional criteria:
    - The to-do list doesn't have login/signup
    - The todos are saved locally in the browser. If the user change the browser or device, the todos is not saved or synced.
    - user can add a due date
    - user can add title and description of the todo
    - user can add labels, separated by comma, starting with #
    - user can delete a todo
    - user can mark as done a todo
    - user can edit the todos.
    - user can mark priority of high, medium and low in todos
    - It doesn't need bulk actions.
    - Export/Import and notifications will be for future evolutions. Just like filters, sorting and project folders.
```

> When using with other LLM Projects, don't forget to add the instructions above in LLM Project Instructions.

Other examples:
- "I want to *create a PRD* for push notifications, using following informations to create it and guide me through the process."
- "Breakdown a *PRD* into epics and stories"
- "Breakdown a *Epic* into stories / tasks"
- "Help me *clarify* my PRD"

---

*Built with ❤️ for product teams who believe in the power of great documentation to potentialize value for business and users.*

## Contributing

This project evolves based on user needs. We welcome your feedback and contributions!

Special thanks to the [spec-kit](https://github.com/github/spec-kit) team for their inspiring work that helped shape this project.


## 📄 License

Open source - use freely for your product documentation needs.

