# Contributing to Ecocee Agent Skills

Thank you for your interest in contributing to this repository. This project is maintained by [Ecocee](https://ecocee.in/) and open to community collaboration. Every contribution — new skills, bug fixes, documentation improvements — is valued.

---

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Ways to Contribute](#ways-to-contribute)
- [Getting Started](#getting-started)
- [Creating a New Skill](#creating-a-new-skill)
- [Skill Quality Checklist](#skill-quality-checklist)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Reporting Issues](#reporting-issues)
- [Community and Discussions](#community-and-discussions)
- [Contact](#contact)

---

## Code of Conduct

By participating in this project, you agree to maintain a respectful, inclusive, and constructive environment. All contributors are expected to:

- Be kind and respectful in all interactions
- Give constructive feedback focused on the work, not the person
- Welcome contributors of all experience levels
- Respect differing viewpoints and approaches

Violations may result in removal from the project. Report concerns to [info@ecocee.in](mailto:info@ecocee.in).

---

## Ways to Contribute

You do not need to be a developer to contribute. Here are ways you can help:

| Type | Description |
|---|---|
| New Skill | Create and submit a brand-new skill |
| Bug Fix | Fix an issue in an existing skill's instructions |
| Improvement | Improve clarity, examples, or guidelines in a skill |
| Documentation | Improve README, guides, or inline documentation |
| Skill Ideas | Open a GitHub Discussion or Issue suggesting a new skill |
| PR Review | Help review other contributors' pull requests |
| Translation | Translate skill descriptions or documentation |

---

## Getting Started

### 1. Fork the Repository

Click the **Fork** button at the top right of this page on GitHub.

### 2. Clone Your Fork

```bash
git clone https://github.com/ecocee/skills.git
cd skills
```

### 3. Create a Branch

Use a descriptive branch name:

```bash
git checkout -b add/resume-builder-skill
git checkout -b fix/email-drafter-examples
git checkout -b docs/update-readme
```

### 4. Make Your Changes

Follow the guidelines below, then commit your work.

### 5. Push and Open a PR

```bash
git push origin your-branch-name
```

Then open a Pull Request from your fork to the `main` branch of `ecocee/skills`.

---

## Creating a New Skill

All skills live inside the `/skills` directory. Each skill must be a folder containing at minimum a `SKILL.md` file.

### Directory Structure

```
skills/
└── your-skill-name/
    ├── SKILL.md          (required)
    ├── README.md         (optional but recommended)
    ├── scripts/          (optional helper scripts)
    └── examples/         (optional examples)
```

### SKILL.md Template

```markdown
---
name: your-skill-name
description: A complete description of what this skill does and when the agent should use it. Be specific — the agent uses this to decide whether to load the skill.
version: 1.0.0
author: Your Name or GitHub handle
license: Apache-2.0
tags: [category, tag1, tag2]
---

# Your Skill Name

A brief intro explaining what this skill enables the agent to do.

## When to Use This Skill

Describe the exact scenarios in which this skill should be triggered.

## Instructions

Step-by-step instructions that the agent will follow when this skill is active.

## Examples

### Example 1: Scenario Name
Input: Description of what the user might say
Output: Description of what the agent should produce

### Example 2: Scenario Name
Input: ...
Output: ...

## Guidelines

- Guideline or constraint 1
- Guideline or constraint 2
- What NOT to do

## Output Format

Describe the expected output format (markdown, JSON, prose, table, etc.)
```

### Frontmatter Fields

| Field | Required | Description |
|---|---|---|
| `name` | Yes | Lowercase, hyphens for spaces (e.g., `resume-builder`) |
| `description` | Yes | Full description — used by the agent to decide when to load the skill |
| `version` | Recommended | Semantic version (e.g., `1.0.0`) |
| `author` | Recommended | Your name or GitHub handle |
| `license` | Recommended | License type (e.g., `Apache-2.0`) |
| `tags` | Optional | Categorization tags |

---

## Skill Quality Checklist

Before submitting, ensure your skill meets these standards.

**Structure**
- [ ] Skill is in its own folder under `/skills/`
- [ ] Folder name matches the `name` field in frontmatter (lowercase, hyphens)
- [ ] `SKILL.md` exists and has valid YAML frontmatter
- [ ] Both `name` and `description` fields are present

**Content Quality**
- [ ] Description is specific enough for the agent to know when to load the skill
- [ ] Instructions are clear, unambiguous, and actionable
- [ ] At least 2 usage examples are included
- [ ] Guidelines cover edge cases and explicitly state what not to do
- [ ] Output format is clearly specified

**Uniqueness**
- [ ] Skill does not duplicate an existing skill in the repository
- [ ] Skill adds genuine value beyond default agent capabilities

**License**
- [ ] Skill is submitted under Apache 2.0 (default) or another compatible license
- [ ] Any third-party content or scripts are properly attributed in `THIRD_PARTY_NOTICES.md`

---

## Submitting a Pull Request

### PR Title Format

```
[New Skill] resume-builder — ATS-friendly resume creator
[Fix] email-drafter — Corrected output format instructions
[Docs] Update CONTRIBUTING.md with translation guide
[Improvement] code-reviewer — Added TypeScript examples
```

### PR Description Template

```markdown
## Summary
Brief description of what this PR adds or changes.

## Skill Name (if applicable)
your-skill-name

## Category
[ ] New Skill  [ ] Bug Fix  [ ] Improvement  [ ] Documentation  [ ] Other

## Testing
How did you test this skill? What prompts or inputs did you use?

## Checklist
- [ ] I have read CONTRIBUTING.md
- [ ] My skill passes the quality checklist
- [ ] I have attributed any third-party content
- [ ] I have tested this skill with at least one compatible agent
```

### Review Process

1. A maintainer from the Ecocee team will review your PR within 5 to 7 business days.
2. You may receive feedback or change requests — please respond promptly.
3. Once approved, your skill will be merged into `main` and credited to you in the commit history and skill frontmatter.

---

## Reporting Issues

Found a bug, unclear instruction, or a skill that is not working as expected?

1. Go to the [Issues tab](../../issues)
2. Click **New Issue**
3. Choose the appropriate template: Bug Report, Skill Suggestion, or Improvement

Please include:
- Skill name
- What you expected versus what happened
- The prompt or input you used
- The agent and environment you tested with (Claude.ai, Claude Code, VS Code, Cursor, etc.)

---

## Community and Discussions

Have a skill idea or want to discuss approaches? Use [GitHub Discussions](../../discussions):

| Category | Use For |
|---|---|
| Ideas | Propose new skills before building them |
| Q&A | Ask questions about skill creation |
| Show and Tell | Share things you have built with skills |
| Announcements | Follow for updates from the Ecocee team |

---

## Contact

For partnership inquiries, enterprise skill development, or any questions about this repository:

- Email: [info@ecocee.in](mailto:info@ecocee.in)
- Website: [ecocee.in](https://ecocee.in/)
- LinkedIn: [linkedin.com/company/ecocee](https://www.linkedin.com/company/ecocee)

---

Maintained and developed by [Ecocee](https://ecocee.in/) — Embedded Systems, IoT and AI Solutions, Kerala, India.
