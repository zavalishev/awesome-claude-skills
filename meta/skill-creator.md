---
name: skill-creator
description: "Guide for creating effective skills that extend Claude's capabilities with specialized knowledge, workflows, or tool integrations."
source: https://github.com/anthropics/skills
---

# Skill Creator

Guide for creating effective skills.

## About Skills

Skills are modular, self-contained packages that extend Claude's capabilities by providing specialized knowledge, workflows, and tools.

### What Skills Provide

1. **Specialized workflows** - Multi-step procedures for specific domains
2. **Tool integrations** - Instructions for working with specific file formats or APIs
3. **Domain expertise** - Company-specific knowledge, schemas, business logic
4. **Bundled resources** - Scripts, references, and assets for complex tasks

## Core Principles

### Concise is Key

The context window is a public good. Only add context Claude doesn't already have.

**Default assumption: Claude is already very smart.**

### Anatomy of a Skill

```
skill-name/
├── SKILL.md (required)
│   ├── YAML frontmatter (name, description)
│   └── Markdown instructions
└── Bundled Resources (optional)
    ├── scripts/      - Executable code (Python/Bash)
    ├── references/   - Documentation to load as needed
    └── assets/       - Files used in output (templates, icons)
```

### Progressive Disclosure

Skills use a three-level loading system:

1. **Metadata (name + description)** - Always in context (~100 words)
2. **SKILL.md body** - When skill triggers (<5k words)
3. **Bundled resources** - As needed by Claude

## Skill Creation Process

### Step 1: Understand with Concrete Examples
- "What functionality should this skill support?"
- "Can you give examples of how this skill would be used?"
- "What would a user say that should trigger this skill?"

### Step 2: Plan Reusable Contents
Analyze each example:
1. Consider how to execute from scratch
2. Identify what scripts, references, and assets would help

### Step 3: Initialize the Skill
```bash
scripts/init_skill.py <skill-name> --path <output-directory>
```

### Step 4: Edit the Skill
- Start with reusable resources (scripts/, references/, assets/)
- Update SKILL.md with frontmatter and instructions
- Test added scripts by actually running them

### Step 5: Package the Skill
```bash
scripts/package_skill.py <path/to/skill-folder>
```

### Step 6: Iterate
1. Use the skill on real tasks
2. Notice struggles or inefficiencies
3. Identify how SKILL.md should be updated
4. Implement changes and test again

## What NOT to Include

- README.md
- INSTALLATION_GUIDE.md
- CHANGELOG.md
- User-facing documentation

The skill should only contain information needed for an AI agent to do the job.

## Frontmatter Guidelines

```yaml
---
name: skill-name
description: "What the skill does AND when to use it. Include triggers/contexts."
---
```

The description is the primary triggering mechanism — Claude uses it to decide when to load the skill.
