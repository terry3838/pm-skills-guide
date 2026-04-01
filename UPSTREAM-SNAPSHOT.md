# Upstream Snapshot — pm-skills

- source repo: `https://github.com/phuryn/pm-skills.git`
- synced commit: `36ccefdc6c2e00d7c0c12cb0a52bf93e8ec50da4`
- guide repo: `pm-skills-guide`

## 원본 한줄 요약

![GitHub stars](https://img.shields.io/github/stars/phuryn/pm-skills) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/CONTRIBUTING.md)

## top-level structure

- `.claude-plugin/`
- `.docs/`
- `CONTRIBUTING.md`
- `LICENSE`
- `pm-data-analytics/`
- `pm-execution/`
- `pm-go-to-market/`
- `pm-market-research/`
- `pm-marketing-growth/`
- `pm-product-discovery/`
- `pm-product-strategy/`
- `pm-toolkit/`
- `README.md`
- `validate_plugins.py`

## README excerpt

```md
![GitHub stars](https://img.shields.io/github/stars/phuryn/pm-skills)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)](https://github.com/phuryn/pm-skills/blob/main/CONTRIBUTING.md)

# PM Skills Marketplace: The AI Operating System for Better Product Decisions

> 65 PM skills and 36 chained workflows across 8 plugins. Claude Code, Cowork, and more. From discovery to strategy, execution, launch, and growth. 

![Plugin overview](.docs/images/plugins-overview.webp)

Designed for Claude Code and Cowork. Skills compatible with other AI assistants.

## Start Here

New idea? → `/discover`  
Need strategic clarity? → `/strategy`  
Writing a PRD? → `/write-prd`  
Planning a launch? → `/plan-launch`  
Defining metrics? → `/north-star`

If this project helps you, ⭐ the repo.

## Why PM Skills Marketplace?

Generic AI gives you text. PM Skills Marketplace gives you structure.

Each skill encodes a proven PM framework — discovery, assumption mapping, prioritization, strategy — and walks you through it step by step. You get the rigor of Teresa Torres, Marty Cagan, and Alberto Savoia built into your daily workflow, not sitting on a bookshelf.

The result: better product decisions, not just faster documents.

## How It Works (Skills, Commands, Plugins)

**Skills** are the building blocks of the marketplace. Each skill gives Claude domain knowledge, analytical frameworks, or a guided workflow for a specific PM task. Some skills also work as reusable foundations that multiple commands share. 

Skills are loaded automatically when relevant to the conversation — no explicit invocation needed. If needed (e.g., prioritizing skills over general knowledge), you can **force loading skills** with `/plugin-name:skill-name` or `/skill-name` (Claude will add the prefix).

**Commands** are user-triggered workflows invoked with `/command-name`. They chain one or more skills into an end-to-end process. For example, `/discover` chains four skills together: brainstorm-ideas → identify-assumptions → prioritize-assumptions → brainstorm-experiments.

**Plugins** group related skills and commands into installable packages. Each plugin covers a PM domain — discovery, strategy, execution, and so on. Installing the marketplace gives you all 8 plugins at once.

![How skills work](.docs/images/how-skills-work.webp)

Commands use skills. Some skills serve multiple commands. Some skills (like `prioritization-frameworks` or `opportunity-solution-tree`) are standalone references that Claude draws on whenever relevant — no command needed.

Commands are designed to flow into each other, matching the PM workflow. After any command completes, it suggests relevant next commands — just follow the prompts.

## Installation

### Claude Cowork (recommended for non-developers)

1. Open **Customize** (bottom-left)
2. Go to **Browse plugins** → **Personal** → **+**
3. Select **Add marketplace from GitHub**
4. Enter: `phuryn/pm-skills`

All 8 plugins install automatically. You get both commands (`/discover`, `/strategy`, etc.) and skills.

![Installing PM Skills in Claude Cowork](.docs/images/pm-skills-install.gif)

### Claude Code (CLI)

```bash
# Step 1: Add the marketplace
claude plugin marketplace add phuryn/pm-skills

# Step 2: Install individual plugins
claude plugin install pm-toolkit@pm-skills
claude plugin install pm-product-strategy@pm-skills
claude plugin install pm-product-discovery@pm-skills 
claude plugin install pm-market-research@pm-skills 
claude plugin install pm-data-analytics@pm-skills
claude plugin install pm-marketing-growth@pm-skills
claude plugin install pm-go-to-market@pm-skills
claude plugin install pm-execution@pm-skills
```

### Other AI assistants (skills only)

The `skills/*/SKILL.md` files follow the universal skill format and work with any tool that reads it. Commands (`/slash-commands`) are Claude-specific.
```
