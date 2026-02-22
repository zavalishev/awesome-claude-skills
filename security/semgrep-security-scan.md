---
name: semgrep-security-scan
description: "Run Semgrep static analysis scan on a codebase. Automatically detects languages and uses parallel subagents. Use when asked to scan code for vulnerabilities, run security audit, or perform static analysis."
source: https://github.com/trailofbits/skills
---

# Semgrep Security Scan

Run complete Semgrep scan with automatic language detection, parallel execution, and triage.

## Prerequisites

**Required:** Semgrep CLI
```bash
semgrep --version
```

If not installed: https://semgrep.dev/docs/getting-started/

**Optional:** Semgrep Pro (for cross-file analysis)
```bash
semgrep install-semgrep-pro
```

## When to Use

- Security audit of a codebase
- Finding vulnerabilities before code review
- Scanning for known bug patterns
- First-pass static analysis

## When NOT to Use

- Binary analysis → Use binary analysis tools
- Already have Semgrep CI configured → Use existing pipeline
- Creating custom rules → Use `semgrep-rule-creator` skill

## Orchestration Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│ MAIN AGENT                                                      │
│ 1. Detect languages + check Pro availability                    │
│ 2. Select rulesets based on detection                           │
│ 3. Present plan + rulesets, get approval [⛔ HARD GATE]         │
│ 4. Spawn parallel scan Tasks (with approved rulesets)           │
│ 5. Spawn parallel triage Tasks                                  │
│ 6. Collect and report results                                   │
└─────────────────────────────────────────────────────────────────┘
```

## Basic Usage

**Scan current directory:**
```bash
semgrep scan --config auto
```

**Scan with specific ruleset:**
```bash
semgrep scan --config p/security-audit
```

**Scan specific language:**
```bash
semgrep scan --config p/python
```

## Common Rulesets

| Ruleset | Description |
|---------|-------------|
| `p/security-audit` | General security issues |
| `p/owasp-top-ten` | OWASP Top 10 vulnerabilities |
| `p/ci` | CI/CD pipeline checks |
| `p/python` | Python-specific rules |
| `p/javascript` | JavaScript/TypeScript rules |
| `p/golang` | Go-specific rules |
| `p/rust` | Rust-specific rules |

## Output Formats

```bash
# JSON output for parsing
semgrep scan --config auto --json > results.json

# SARIF for IDE integration
semgrep scan --config auto --sarif > results.sarif

# Text summary
semgrep scan --config auto --text
```

## Triage Process

1. **High severity first** - Focus on critical/high findings
2. **Group by rule** - Similar issues often have same root cause
3. **Check false positives** - Some patterns trigger on safe code
4. **Verify exploitability** - Not all findings are exploitable

## Integration with Other Tools

- **CodeQL** - Deeper semantic analysis
- **SARIF parsing** - IDE integration
- **CI/CD** - Automated scanning in pipelines
