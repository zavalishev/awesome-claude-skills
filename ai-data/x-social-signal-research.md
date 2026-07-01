---
name: x-social-signal-research
description: Use when researching current X/Twitter market signals, audience language, competitor activity, content angles, or launch feedback with the Hermes Tweet plugin for Hermes Agent.
license: MIT
metadata:
  author: https://github.com/Xquik-dev/hermes-tweet
  version: "1.0.0"
  domain: social-research
  triggers: X, Twitter, social listening, market signals, competitor research, audience research, content planning, launch monitoring
  role: researcher
  scope: signal-analysis
  output-format: brief
  related-skills: prompt-engineer, rag-architect
---

# X Social Signal Research

Use Hermes Tweet when a task needs current X/Twitter evidence for market, content, competitor, audience, or launch decisions.

## When to Use This Skill

- Checking whether a topic has recent X/Twitter engagement
- Finding audience language before writing posts or landing-page copy
- Comparing competitor positioning and launch reactions
- Monitoring public discussion around an incident, product, or campaign
- Preparing a short social signal brief for a Hermes Agent workflow

## Required Tooling

Hermes Tweet is a Hermes Agent plugin:

- Repository: https://github.com/Xquik-dev/hermes-tweet
- Install: `hermes plugins install Xquik-dev/hermes-tweet`
- Reads require `XQUIK_API_KEY`
- Actions require `XQUIK_API_KEY` and `HERMES_TWEET_ENABLE_ACTIONS=true`

## Workflow

1. Define the decision the research must support.
2. Turn it into 2-4 focused X/Twitter queries.
3. Use read-only Hermes Tweet tools unless the user explicitly asks for an action.
4. Group findings by signal type: topics, people, objections, language, examples.
5. Separate observed signals from interpretation.
6. End with the next query or action that would reduce uncertainty.

## Output Template

```markdown
## What I Checked
- Query/topic:
- Time/context:

## Signals
- Topic:
- Audience language:
- Competitor or creator activity:

## Interpretation
- Strong signal:
- Weak signal:
- Uncertainty:

## Next Step
- Recommended follow-up:
```

## Guardrails

- Do not invent live social evidence.
- Do not post, like, follow, or delete unless action tools are enabled and requested.
- Keep API keys in environment variables.
- Mention uncertainty when results are sparse, stale, or ambiguous.
