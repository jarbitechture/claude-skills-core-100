---
name: claude-skills
description: A collection of 1,253 Claude Code skills covering automation, development, security, infrastructure, reasoning, and creative workflows. Use this as a skill discovery and installation hub.
version: 1.0.0
author: jarbitechture
---

# Claude Skills Collection

The largest personal collection of Claude Code skills — 1,253 markdown-based prompt modules that extend Claude's capabilities across every major domain.

## Skill Categories

| Category | Count | Examples |
|----------|-------|---------|
| SaaS & API Automations | 910 | Slack, Notion, GitHub, Salesforce, Stripe, Shopify |
| Azure SDK & Cloud | 97 | Cosmos DB, Key Vault, Event Hubs, AI Services |
| Routers & Orchestrators | 27 | meta-router, agents-router, reasoning-router |
| Google Integrations | 24 | Gmail, Drive, Calendar, Maps, BigQuery, Ads |
| Development & Code Quality | 20+ | TDD, refactoring, test generation, API design |
| Agent & Multi-Agent Frameworks | 16 | DSPy, multi-agent patterns, agent evaluation |
| Zoho Suite | 14 | CRM, Books, Desk, Mail, Inventory, Bigin |
| Reasoning & Cognitive Tools | 11 | think, reason, dialectical, critique, constraints |
| Infrastructure & DevOps | 10+ | Terraform, K8s, CI/CD, Cloudflare, Vercel |
| AI & ML Tools | 15+ | HF model trainer, DSPy, prompt engineering |
| Security & Vulnerability | 8 | Semgrep, CodeQL, threat modeling, OWASP |
| Obsidian Knowledge Mgmt | 8 | Vault workflows, batch ops, data import |
| Creative & Media | 10+ | Suno songs, podcasts, image gen, video |
| File Format Processors | 7 | PDF, DOCX, PPTX, XLSX, CSV, JSON Canvas |
| Notion Workflows | 5 | Knowledge capture, meeting intel, spec-to-code |

## Installation

### Install a Single Skill

```bash
git clone https://github.com/jarbitechture/claude-skills.git ~/claude-skills
cp -r ~/claude-skills/skills/<skill-name> ~/.claude/skills/
```

### Install All Skills

```bash
git clone https://github.com/jarbitechture/claude-skills.git ~/claude-skills
ln -s ~/claude-skills/skills/* ~/.claude/skills/
```

### Install by Category

```bash
# Security skills
for skill in vulnerability-scanning security-threat-model security-best-practices security-ownership-map osgrep; do
  cp -r ~/claude-skills/skills/$skill ~/.claude/skills/
done

# Reasoning skills
for skill in think reason dialectical critique hierarchical-reasoning thought-based-reasoning constraints textbook-grounding grounding-router; do
  cp -r ~/claude-skills/skills/$skill ~/.claude/skills/
done
```

## Skill Structure

Each skill follows a standard layout:

```
skill-name/
├── SKILL.md        # Core instructions, workflows, trigger conditions
├── CLAUDE.md       # Optional project-level overrides
├── references/     # Supporting docs, API schemas, examples
└── scripts/        # Executable helpers (Python, Node, shell)
```

## How Skills Work

Skills are loaded automatically by Claude Code based on context, or invoked explicitly via `/skill-name`. When triggered, Claude receives the skill's specialized instructions and can execute its defined workflows.

```
User: "Send a Slack message to #general"
  → Claude loads slack-automation skill
  → Skill provides API surface, auth flow, tool schemas
  → Claude executes the workflow
  → Message sent
```

## Sources & Attribution

| Source | Skills |
|--------|--------|
| [antonbabenko/terraform-skill](https://github.com/antonbabenko/terraform-skill) | Terraform/OpenTofu |
| [trailofbits/skills](https://github.com/trailofbits/skills) | Security scanning, PBT |
| [ahmedasmar/devops-claude-skills](https://github.com/ahmedasmar/devops-claude-skills) | DevOps, K8s |
| [andronics/claude-plugin-adr](https://github.com/andronics/claude-plugin-adr) | Architecture Decision Records |
| [levnikolaevich/claude-code-skills](https://github.com/levnikolaevich/claude-code-skills) | Development tools |
| [QuestForTech-Investments/claude-code-skills](https://github.com/QuestForTech-Investments/claude-code-skills) | Automation skills |
| [Composio](https://composio.dev) | SaaS integration toolkits |
| Community & custom | Reasoning, orchestration, creative |
