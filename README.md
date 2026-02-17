> **Note:** This repository is maintained and developed by [Ecocee](https://ecocee.in/). For information about the Agent Skills standard, see [agentskills.io](http://agentskills.io).

<div align="center">

<img src="https://ecocee.in/logo_black.png" alt="Ecocee Logo" width="160"/>

# Ecocee Agent Skills

**A community-driven, open repository of Agent Skills — compatible with Claude, VS Code, Cursor, Windsurf, Antigravity, Claude Code, and any agent that supports the Agent Skills standard.**

[![Stars](https://img.shields.io/github/stars/ecocee/skills?style=flat-square)](https://github.com/ecocee/skills/stargazers)
[![Forks](https://img.shields.io/github/forks/ecocee/skills?style=flat-square)](https://github.com/ecocee/skills/forks)
[![License](https://img.shields.io/badge/license-Apache%202.0-green?style=flat-square)](./LICENSE)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen?style=flat-square)](./CONTRIBUTING.md)

</div>

---

## What Are Skills?

Skills are folders of instructions, scripts, and resources that an AI agent loads dynamically to improve performance on specialized tasks. Skills teach agents how to complete specific tasks in a repeatable, reliable way — whether that's generating embedded system documentation, analyzing IoT sensor data, writing firmware specifications, or automating enterprise workflows.

This repository follows the open [Agent Skills standard](http://agentskills.io), which means skills here work across any compatible agent and development environment — not just one tool or platform.

For more information, check out:
- [What are skills?](https://support.claude.com/en/articles/12512176-what-are-skills)
- [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)
- [How to create custom skills](https://support.claude.com/en/articles/12512198-creating-custom-skills)
- [Agent Skills standard specification](http://agentskills.io)
- [Equipping agents for the real world with Agent Skills](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

---

## Compatible Agents and Environments

Skills in this repository are designed to work with any agent or environment that supports the Agent Skills standard, including:

- Claude (claude.ai)
- Claude Code
- VS Code (via compatible extensions)
- Cursor
- Windsurf
- Antigravity
- Any agent supporting the SKILL.md specification

---

## About This Repository

This repository contains community skills that demonstrate what is possible with the Agent Skills system. Skills span a wide range of domains:

| Category | Examples |
|---|---|
| Embedded and IoT | Firmware doc generator, IoT schema builder, RTOS config helper |
| AI and ML | Model card writer, dataset analyzer, prompt optimizer |
| Enterprise | Meeting summarizer, email drafter, product roadmap creator |
| Documents | Resume builder, technical spec writer, report generator |
| Development | Code reviewer, API doc generator, test case creator |
| Creative and Design | UX copy writer, social media creator, pitch deck builder |

Each skill is self-contained in its own folder with a `SKILL.md` file that the agent reads and follows.

---

## Repository Structure

```
ecocee-skills/
├── README.md
├── CONTRIBUTING.md
├── THIRD_PARTY_NOTICES.md
├── LICENSE
├── skills/
│   ├── resume-builder/
│   │   └── SKILL.md
│   ├── firmware-doc-generator/
│   │   └── SKILL.md
│   ├── iot-schema-builder/
│   │   └── SKILL.md
│   ├── code-reviewer/
│   │   └── SKILL.md
│   └── ...
├── spec/
└── template/
    └── SKILL.md
```

---

## Try It Out

### Claude.ai

All skills in this repository can be uploaded to Claude.ai (paid plans). Follow the instructions in [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude#h_a4222fa77b).

### Claude Code

Register this repository as a Claude Code Plugin marketplace:

```bash
/plugin marketplace add ecocee/skills
```

Then install a skill set:

```bash
/plugin install document-skills@ecocee-skills
/plugin install example-skills@ecocee-skills
```

After installing, you can use a skill by mentioning it directly. For example: "Use the firmware-doc skill to generate documentation for this header file."

### VS Code and Other Editors

Place any skill folder inside your project or workspace and configure your agent extension to load skills from the `/skills` directory. Refer to your specific extension's documentation for the exact setup path.

### Claude API

Use skills via the Claude API. See the [Skills API Quickstart](https://docs.claude.com/en/api/skills-guide#creating-a-skill) for details.

---

## Creating a Skill

Skills are simple to create — just a folder with a `SKILL.md` file. Use the template in [`/template`](./template/SKILL.md) as your starting point:

```markdown
---
name: my-skill-name
description: A clear description of what this skill does and when to use it
---

# My Skill Name

[Add your instructions here that the agent will follow when this skill is active]

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

**Required frontmatter fields:**
- `name` — Unique identifier (lowercase, hyphens for spaces)
- `description` — Complete description of what the skill does and when it should be triggered

---

## Skills List

| # | Skill | Description |
|---|---|---|
| 1 | `resume-builder` | Creates ATS-friendly, professional resumes |
| 2 | `code-reviewer` | Structured pull request and code review feedback |
| 3 | `seo-writer` | SEO-optimized blog and web content |
| 4 | `sql-query-helper` | Generates and explains SQL queries |
| 5 | `email-drafter` | Professional email writing for any context |
| 6 | `meeting-summarizer` | Summarizes meeting transcripts with action items |
| 7 | `api-doc-generator` | Auto-generates clean API documentation |
| 8 | `data-analyst` | Analyzes CSV and Excel datasets with insights |
| 9 | `legal-clause-checker` | Reviews contracts and flags risk areas |
| 10 | `social-media-creator` | Creates posts for LinkedIn, Twitter, Instagram |
| 11 | `bug-report-writer` | Structures clear and reproducible bug reports |
| 12 | `product-roadmap` | Creates product roadmap documents |
| 13 | `firmware-doc-generator` | Generates firmware and embedded system documentation |
| 14 | `iot-schema-builder` | Builds IoT data schemas and device specifications |
| 15 | `test-case-generator` | Generates unit and integration test cases |
| 16 | `lesson-plan-creator` | Creates structured lesson and course plans |
| 17 | `startup-pitch-writer` | Writes compelling investor pitch decks |
| 18 | `devops-runbook` | Creates detailed DevOps runbook documents |
| 19 | `ux-copy-writer` | Writes UI/UX microcopy and interface text |
| 20 | `research-paper-helper` | Structures and formats academic research papers |

---

## Contributing

Contributions are welcome from the community. Whether it is a new skill, a bug fix, or an improvement to an existing one, all contributions are appreciated.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for full guidelines.

---

## Disclaimer

**These skills are provided for demonstration and educational purposes only.** While some capabilities may be available across agents, implementations and behaviors may differ depending on the agent and environment. Always test skills thoroughly in your own environment before relying on them for critical tasks.

---

## License

Most skills in this repository are open source under the [MIT License](./LICENSE).

Some skills marked as source-available are shared for reference only. See individual skill folders for their specific license.

---

## About Ecocee

This repository is maintained and developed by **Ecocee**, an MSME specializing in Embedded Systems, IoT, and AI Solutions based in Kerala, India.

| | |
|---|---|
| Website | [ecocee.in](https://ecocee.in/) |
| Email | [info@ecocee.in](mailto:info@ecocee.in) |
| LinkedIn | [linkedin.com/company/ecocee](https://www.linkedin.com/company/ecocee) |


© 2026–27 Ecocee. All rights reserved.
