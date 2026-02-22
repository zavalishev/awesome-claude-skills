---
name: mcp-builder
description: "Guide for creating high-quality MCP (Model Context Protocol) servers that enable LLMs to interact with external services through well-designed tools."
source: https://github.com/anthropics/skills
---

# MCP Server Development Guide

## Overview

Create MCP servers that enable LLMs to interact with external services through well-designed tools.

**Recommended stack:**
- **Language**: TypeScript (best SDK support)
- **Transport**: Streamable HTTP for remote servers, stdio for local

## High-Level Workflow

### Phase 1: Deep Research and Planning

#### 1.1 Understand Modern MCP Design

**API Coverage vs. Workflow Tools:**
Balance comprehensive API endpoint coverage with specialized workflow tools.

**Tool Naming:**
Use consistent prefixes (e.g., `github_create_issue`, `github_list_repos`).

**Actionable Error Messages:**
Guide agents toward solutions with specific suggestions.

#### 1.2 Study MCP Protocol Documentation

Start with sitemap: `https://modelcontextprotocol.io/sitemap.xml`

Key pages:
- Specification overview and architecture
- Transport mechanisms (streamable HTTP, stdio)
- Tool, resource, and prompt definitions

#### 1.3 Study Framework Documentation

**TypeScript SDK:**
```
https://raw.githubusercontent.com/modelcontextprotocol/typescript-sdk/main/README.md
```

**Python SDK:**
```
https://raw.githubusercontent.com/modelcontextprotocol/python-sdk/main/README.md
```

### Phase 2: Implementation

#### 2.1 Set Up Project Structure

See language-specific guides for project setup.

#### 2.2 Implement Core Infrastructure

- API client with authentication
- Error handling helpers
- Response formatting (JSON/Markdown)
- Pagination support

#### 2.3 Implement Tools

For each tool:

**Input Schema:**
- Use Zod (TypeScript) or Pydantic (Python)
- Include constraints and clear descriptions

**Output Schema:**
- Define `outputSchema` where possible
- Use `structuredContent` in tool responses

**Annotations:**
- `readOnlyHint`: true/false
- `destructiveHint`: true/false
- `idempotentHint`: true/false

### Phase 3: Review and Test

- No duplicated code (DRY)
- Consistent error handling
- Full type coverage
- Clear tool descriptions

**TypeScript:**
```bash
npm run build
npx @modelcontextprotocol/inspector
```

**Python:**
```bash
python -m py_compile your_server.py
```

### Phase 4: Create Evaluations

Create 10 evaluation questions:
- Independent, read-only, complex, realistic
- Single, verifiable answer

```xml
<evaluation>
  <qa_pair>
    <question>Your complex question here?</question>
    <answer>Expected answer</answer>
  </qa_pair>
</evaluation>
```
