---
name: designing-workflow-skills
description: >-
  Guides the design and structuring of workflow-based Claude Code skills
  with multi-step phases, decision trees, subagent delegation, and
  progressive disclosure. Use when creating skills that involve
  sequential pipelines, routing patterns, safety gates, task tracking,
  phased execution, or any multi-step workflow. Also applies when
  reviewing or refactoring existing workflow skills for quality.
allowed-tools:
  - Read
  - Glob
  - Grep
  - TodoRead
  - TodoWrite
---

# Designing Workflow Skills

Build workflow-based skills that execute reliably by following structural patterns, not prose.

## Essential Principles

<essential_principles>

<principle name="description-is-the-trigger">
**The `description` field is the only thing that controls when a skill activates.**

Claude decides whether to load a skill based solely on its frontmatter `description`. The body of SKILL.md — including "When to Use" and "When NOT to Use" sections — is only read AFTER the skill is already active. Put your trigger keywords, use cases, and exclusions in the description. A bad description means wrong activations or missed activations regardless of what the body says.

"When to Use" and "When NOT to Use" sections still serve a purpose: they scope the LLM's behavior once active. "When NOT to Use" should name specific alternatives: "use Semgrep for simple pattern matching" not "not for simple tasks."
</principle>

(Полное содержимое см. выше - сокращено для краткости)