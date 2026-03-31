# Contributing to CmdHub Documentation

Thank you for your interest in contributing to the **CmdHub Documentation**! This guide will help you get started with editing and improving our documentation for CmdHub.

We are excited about your participation. By contributing, you are helping us build a better resource for developers creating commands for the Discord App Bot Maker.

## 📋 Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Features](#suggesting-features)
  - [Improving Documentation](#improving-documentation)
- [Documentation Setup](#documentation-setup)
- [Style Guide](#style-guide)
- [Commit Guidelines](#commit-guidelines)

---

## Code of Conduct

Please read and follow our [Contributor Covenant](https://www.contributor-covenant.org/version/2/1/code_of_conduct.html). All CmdHub contributors are expected to uphold a standard of professionalism. Since we deal with Discord Data and Login, please ensure your contributions comply with **Discord's Developer Policies**.

---

## How to Contribute

### Reporting Bugs
Before creating bug reports, check existing issues on the [CmdHub Issues Board](#). 
- Use a clear and descriptive title (e.g., "Error 404 on Command View Page").
- Describe the exact steps that reproduce the problem in as many details as possible.
- Mention which version of CmdHub documentation you are using.

### Suggesting Features
If you have suggestions for new features, please check out the [Feature Requests](#) board first. 
- Provide a clear title and description.
- Explain why this feature would be valuable to **Command Creators** or **Bot Users**.

### Improving Documentation
Documentation is the #1 priority for this repository. You can improve it by:
- Correcting grammatical or spelling errors.
- Adding examples of command JSON data usage.
- Clarifying instructions on how to tag or upload commands.
- Fixing broken links (e.g., GitHub repo placeholders).

---

## Documentation Setup

To run the documentation site locally and preview changes, you need Python and `mkdocs` installed.

1.  **Install MkDocs & Extensions:**
    ```bash
    pip install mkdocs mkdocs-material mkdocs-awesome-pages-plugin
    ```
2.  **Install Local Dependencies:**
    ```bash
    pip install -r requirements-docs.txt
    ```
3.  **Run the Docs Server:**
    Navigate to your docs directory and run:
    ```bash
    mkdocs serve
    ```
4.  **Open the Site:**
    Open [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser to view changes live.

---

## Style Guide

To maintain consistency within the MkDocs site, please adhere to these guidelines:

### Markdown Rules
- **No Tabs:** Use spaces for indentation only. MkDocs often fails to render tabs correctly in YAML frontmatter or markdown blocks.
- **Frontmatter:** If editing a page that requires metadata (like navigation), ensure your YAML frontmatter is indented properly with 2 spaces.
- **Headings:** Maintain a hierarchy (e.g., don't jump from `H1` directly to `H3`).
- **Code Blocks:** Use specific highlighting where possible. For JSON command data, use the `json` language identifier:
    ```json title="Example Command Payload"
    {
      "name": "hello",
      "version": "v1.0.0",
      "raw_data": "{}"
    }
    ```

### Linking Commands
When referencing specific command types (e.g., Slash, Context, Message), use the standard CmdHub badges defined in the UI documentation. Do not create new terminology for existing badge systems without approval from maintainers.

### Tone and Voice
- **Tone:** Professional yet enthusiastic.
- **Audience:** Primarily developers building Discord bots using the App Bot Maker. Avoid overly casual slang.
- **Permissions:** If a section requires login (e.g., "User Profile"), clarify that it applies to authenticated users, as per the site logic.

---

## Commit Guidelines

Please follow [Conventional Commits](https://www.conventionalcommits.org/) for your commits affecting the docs repository:

| Type | Example Subject | Description |
| :--- | :--- | :--- |
| `docs` | `docs: update README` | Documentation changes (non-code). |
| `feat` | `feat(cmd): add new upload form field` | New feature added to the docs. |
| `fix` | `fix(nav): correct broken nav link` | Bug fixes for the MkDocs site. |
| `style` | `style: update markdown spacing` | Code styling (whitespace, formatting). |
| `test` | `test: add unit test for mkdocs` | Adding tests to the docs pipeline. |

**Never commit directly to main.** Always create a Pull Request and ensure CI checks pass before merging.

---

## 📢 Discord TOS & Security Reminder

Since CmdHub handles **Discord Login** and command data:
- Do not write documentation that encourages sharing API Tokens or sensitive keys in GitHub repositories.
- Ensure all code snippets for Discord integration respect the official Discord Developer Portal security practices.
- Contributors must agree to abide by [Discord's Terms of Service](https://discord.com/terms) when contributing content about Discord interactions.

---

## Questions?

If you have questions or need help with the MkDocs setup, please open a GitHub Discussion or comment on an existing issue. We appreciate your contributions!
