# Skills Library

Локальная библиотека скиллов для Claude Code. **81 скилл**.

## Использование

1. Скопируй нужный скилл в `.claude/commands/` своего проекта
2. Или добавь содержимое в `CLAUDE.md`

---

## Каталог скиллов

### Development Process (14)

| Скилл | Файл | Описание |
|-------|------|----------|
| Brainstorming | [brainstorming.md](./development-process/brainstorming.md) | Discovery фаза — сократический диалог перед дизайном |
| Writing Plans | [writing-plans.md](./development-process/writing-plans.md) | Создание детальных планов с bite-sized задачами |
| Executing Plans | [executing-plans.md](./development-process/executing-plans.md) | Batch execution планов с checkpoints |
| Finishing Branch | [finishing-a-development-branch.md](./development-process/finishing-a-development-branch.md) | Merge/PR/cleanup workflow |
| Test-Driven Development | [test-driven-development.md](./development-process/test-driven-development.md) | RED-GREEN-REFACTOR цикл |
| Systematic Debugging | [systematic-debugging.md](./development-process/systematic-debugging.md) | 4-фазный процесс поиска root cause |
| Verification | [verification-before-completion.md](./development-process/verification-before-completion.md) | Проверка перед заявлением о завершении |
| Subagent Development | [subagent-driven-development.md](./development-process/subagent-driven-development.md) | Execution планов через субагентов с code review |
| Dispatching Agents | [dispatching-parallel-agents.md](./development-process/dispatching-parallel-agents.md) | Параллельный запуск независимых агентов |
| Git Worktrees | [using-git-worktrees.md](./development-process/using-git-worktrees.md) | Изолированные рабочие области через git worktrees |
| Feature Forge | [feature-forge.md](./development-process/feature-forge.md) | End-to-end feature implementation |
| Spec Miner | [spec-miner.md](./development-process/spec-miner.md) | Извлечение требований из документации |
| The Fool | [the-fool.md](./development-process/the-fool.md) | Fresh perspective, questioning assumptions |
| Doc Co-Authoring | [doc-coauthoring.md](./development-process/doc-coauthoring.md) | Совместное написание документации |

### Code Quality & Review (10)

| Скилл | Файл | Описание |
|-------|------|----------|
| Make No Mistakes | [make-no-mistakes.md](./code-quality/make-no-mistakes.md) | Повышает точность — проверка перед каждым ответом |
| Code Reviewer | [code-reviewer.md](./code-quality/code-reviewer.md) | Comprehensive code review |
| Code Documenter | [code-documenter.md](./code-quality/code-documenter.md) | Документирование кода |
| Requesting Review | [requesting-code-review.md](./code-quality/requesting-code-review.md) | Запрос code review |
| Receiving Review | [receiving-code-review.md](./code-quality/receiving-code-review.md) | Обработка feedback от review |
| Test Master | [test-master.md](./code-quality/test-master.md) | Comprehensive testing strategies |
| Property-Based Testing | [property-based-testing.md](./code-quality/property-based-testing.md) | Генеративное тестирование свойств |
| Testing Handbook | [testing-handbook-skills.md](./code-quality/testing-handbook-skills.md) | Best practices тестирования |
| Differential Review | [differential-review.md](./code-quality/differential-review.md) | Security-focused diff review |
| Second Opinion | [second-opinion.md](./code-quality/second-opinion.md) | Альтернативный взгляд на решение |

### Security (10)

| Скилл | Файл | Описание |
|-------|------|----------|
| Semgrep Scan | [semgrep-security-scan.md](./security/semgrep-security-scan.md) | Static analysis, поиск уязвимостей |
| Security Reviewer | [security-reviewer.md](./security/security-reviewer.md) | Security-focused code review |
| Secure Code Guardian | [secure-code-guardian.md](./security/secure-code-guardian.md) | Secure coding practices |
| Fullstack Guardian | [fullstack-guardian.md](./security/fullstack-guardian.md) | Full-stack security review |
| Audit Context | [audit-context-building.md](./security/audit-context-building.md) | Подготовка контекста для security audit |
| Sharp Edges | [sharp-edges.md](./security/sharp-edges.md) | Выявление опасных паттернов |
| Insecure Defaults | [insecure-defaults.md](./security/insecure-defaults.md) | Поиск небезопасных настроек по умолчанию |
| Variant Analysis | [variant-analysis.md](./security/variant-analysis.md) | Поиск похожих уязвимостей |
| Semgrep Rule Creator | [semgrep-rule-creator.md](./security/semgrep-rule-creator.md) | Создание кастомных Semgrep правил |
| Firebase APK Scanner | [firebase-apk-scanner.md](./security/firebase-apk-scanner.md) | Сканирование APK на Firebase уязвимости |

### API & Backend (6)

| Скилл | Файл | Описание |
|-------|------|----------|
| API Designer | [api-designer.md](./api-backend/api-designer.md) | REST/GraphQL API design, OpenAPI specs |
| FastAPI Expert | [fastapi-expert.md](./api-backend/fastapi-expert.md) | FastAPI best practices |
| NestJS Expert | [nestjs-expert.md](./api-backend/nestjs-expert.md) | NestJS architecture |
| WebSocket Engineer | [websocket-engineer.md](./api-backend/websocket-engineer.md) | Real-time WebSocket apps |
| Microservices Architect | [microservices-architect.md](./api-backend/microservices-architect.md) | Microservices design |
| Architecture Designer | [architecture-designer.md](./api-backend/architecture-designer.md) | System architecture |

### Frontend (4)

| Скилл | Файл | Описание |
|-------|------|----------|
| Frontend Design | [frontend-design.md](./frontend/frontend-design.md) | Distinctive UI без "AI slop" |
| React Expert | [react-expert.md](./frontend/react-expert.md) | React best practices |
| Next.js Developer | [nextjs-developer.md](./frontend/nextjs-developer.md) | Next.js patterns |
| React Native Expert | [react-native-expert.md](./frontend/react-native-expert.md) | Cross-platform mobile |

### Infrastructure & DevOps (7)

| Скилл | Файл | Описание |
|-------|------|----------|
| DevOps Engineer | [devops-engineer.md](./infrastructure/devops-engineer.md) | CI/CD, automation |
| Cloud Architect | [cloud-architect.md](./infrastructure/cloud-architect.md) | Cloud infrastructure design |
| Kubernetes Specialist | [kubernetes-specialist.md](./infrastructure/kubernetes-specialist.md) | K8s orchestration |
| Terraform Engineer | [terraform-engineer.md](./infrastructure/terraform-engineer.md) | Infrastructure as Code |
| Monitoring Expert | [monitoring-expert.md](./infrastructure/monitoring-expert.md) | Observability, metrics, alerts |
| DevContainer Setup | [devcontainer-setup.md](./infrastructure/devcontainer-setup.md) | VS Code devcontainers |
| Git Cleanup | [git-cleanup.md](./infrastructure/git-cleanup.md) | Git repository maintenance |

### Database (3)

| Скилл | Файл | Описание |
|-------|------|----------|
| PostgreSQL Pro | [postgres-pro.md](./database/postgres-pro.md) | PostgreSQL optimization |
| Database Optimizer | [database-optimizer.md](./database/database-optimizer.md) | Query optimization |
| SQL Pro | [sql-pro.md](./database/sql-pro.md) | Advanced SQL patterns |

### Languages (5)

| Скилл | Файл | Описание |
|-------|------|----------|
| Python Pro | [python-pro.md](./languages/python-pro.md) | Pythonic patterns |
| TypeScript Pro | [typescript-pro.md](./languages/typescript-pro.md) | TypeScript best practices |
| Go Pro | [golang-pro.md](./languages/golang-pro.md) | Idiomatic Go |
| Swift Expert | [swift-expert.md](./languages/swift-expert.md) | Swift/iOS development |
| Modern Python | [modern-python.md](./languages/modern-python.md) | Python 3.10+ features |

### AI & Data (3)

| Скилл | Файл | Описание |
|-------|------|----------|
| RAG Architect | [rag-architect.md](./ai-data/rag-architect.md) | Retrieval-Augmented Generation |
| Prompt Engineer | [prompt-engineer.md](./ai-data/prompt-engineer.md) | LLM prompt optimization |
| Pandas Pro | [pandas-pro.md](./ai-data/pandas-pro.md) | Data manipulation |

### Design & Creative (4)

| Скилл | Файл | Описание |
|-------|------|----------|
| Algorithmic Art | [algorithmic-art.md](./design-creative/algorithmic-art.md) | Generative art на p5.js |
| Canvas Design | [canvas-design.md](./design-creative/canvas-design.md) | Постеры, artwork в PNG/PDF |
| GIF Creator | [gif-creator.md](./design-creative/gif-creator.md) | Анимированные GIF для Slack |
| Theme Factory | [theme-factory.md](./design-creative/theme-factory.md) | Темы для презентаций и документов |

### Documents & Office (4)

| Скилл | Файл | Описание |
|-------|------|----------|
| DOCX | [docx.md](./documents/docx.md) | Создание/редактирование Word документов |
| PDF | [pdf.md](./documents/pdf.md) | Работа с PDF файлами |
| PPTX | [pptx.md](./documents/pptx.md) | Создание презентаций |
| XLSX | [xlsx.md](./documents/xlsx.md) | Работа с Excel файлами |

### Testing & Automation (3)

| Скилл | Файл | Описание |
|-------|------|----------|
| Webapp Testing | [webapp-testing.md](./testing-automation/webapp-testing.md) | Тестирование веб-приложений |
| Playwright Automation | [playwright-automation.md](./testing-automation/playwright-automation.md) | Browser automation |
| iOS Simulator | [ios-simulator.md](./testing-automation/ios-simulator.md) | iOS тестирование и автоматизация |

### Tools & CLI (3)

| Скилл | Файл | Описание |
|-------|------|----------|
| CLI Developer | [cli-developer.md](./tools-cli/cli-developer.md) | Command-line tool development |
| GH CLI | [gh-cli.md](./tools-cli/gh-cli.md) | GitHub CLI best practices |
| Web Artifacts Builder | [web-artifacts-builder.md](./tools-cli/web-artifacts-builder.md) | React/Tailwind artifacts для Claude |

### Meta / Skill Creation (5)

| Скилл | Файл | Описание |
|-------|------|----------|
| Skill Creator | [skill-creator.md](./meta/skill-creator.md) | Гайд по созданию новых скиллов |
| MCP Builder | [mcp-builder.md](./meta/mcp-builder.md) | Создание MCP серверов |
| Writing Skills | [writing-skills.md](./meta/writing-skills.md) | TDD для написания скиллов |
| Workflow Skill Design | [workflow-skill-design.md](./meta/workflow-skill-design.md) | Дизайн workflow скиллов |
| Ask Questions | [ask-questions-if-underspecified.md](./meta/ask-questions-if-underspecified.md) | Уточняющие вопросы перед работой |

---

## Структура папок

```
skills/
├── INDEX.md
├── development-process/    # 14 скиллов
├── code-quality/           # 10 скиллов
├── security/               # 10 скиллов
├── api-backend/            # 6 скиллов
├── frontend/               # 4 скилла
├── infrastructure/         # 7 скиллов
├── database/               # 3 скилла
├── languages/              # 5 скиллов
├── ai-data/                # 3 скилла
├── design-creative/        # 4 скилла
├── documents/              # 4 скилла
├── testing-automation/     # 3 скилла
├── tools-cli/              # 3 скилла
└── meta/                   # 5 скиллов
```

---

## Источники

- [anthropics/skills](https://github.com/anthropics/skills) — официальные скиллы от Anthropic
- [obra/superpowers](https://github.com/obra/superpowers) — 20+ battle-tested скиллов
- [trailofbits/skills](https://github.com/trailofbits/skills) — security-focused скиллы
- [Jeffallan/claude-skills](https://github.com/Jeffallan/claude-skills) — 35+ role-based скиллов
- [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) — iOS automation
- [awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) — курируемый список

---

## Добавление нового скилла

1. Создай файл `skill-name.md` в соответствующей папке категории
2. Добавь frontmatter:

```yaml
---
name: skill-name
description: "Краткое описание скилла"
source: "URL источника (опционально)"
---
```

3. Добавь запись в соответствующую категорию в INDEX.md
