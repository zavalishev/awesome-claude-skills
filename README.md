# 🧠 Claude Code Skills Library

Курируемая библиотека **81 скилла** для Claude Code — расширяй возможности AI-ассистента для разработки.

> **Скиллы** — это инструкции и паттерны, которые улучшают работу Claude Code в специфических задачах: от TDD и code review до создания презентаций и security-аудита.

---

## 🚀 Быстрый старт

### Вариант 1: Один скилл
```bash
# Скопируй нужный скилл в проект
cp skills/security/semgrep-security-scan.md .claude/commands/
```

### Вариант 2: Все скиллы
```bash
# Клонируй репозиторий
git clone https://github.com/anthropics/claude-skills-library.git

# Скопируй нужную категорию
cp -r claude-skills-library/security/ .claude/commands/
```

### Вариант 3: Добавь в CLAUDE.md
```markdown
# В файле CLAUDE.md твоего проекта
@security/semgrep-security-scan.md
```

---

## 📚 Источники

Эта библиотека собрана из лучших открытых репозиториев:

| Репозиторий | Описание | Скиллов |
|-------------|----------|---------|
| [anthropics/skills](https://github.com/anthropics/skills) | Официальные скиллы от Anthropic | 11 |
| [obra/superpowers](https://github.com/obra/superpowers) | Battle-tested workflow скиллы | 12 |
| [trailofbits/skills](https://github.com/trailofbits/skills) | Security-focused скиллы от Trail of Bits | 16 |
| [Jeffallan/claude-skills](https://github.com/Jeffallan/claude-skills) | Role-based скиллы для разных специализаций | 34 |
| [conorluddy/ios-simulator-skill](https://github.com/conorluddy/ios-simulator-skill) | iOS automation | 1 |

Также использованы материалы из [awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills).

---

## 📂 Каталог скиллов

### 🔄 Development Process (14 скиллов)

Скиллы для организации процесса разработки — от брейншторма до деплоя.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Brainstorming](./development-process/brainstorming.md)** | Начинаешь новую фичу и нужно обсудить идеи, требования, edge cases |
| **[Writing Plans](./development-process/writing-plans.md)** | Нужно разбить большую задачу на конкретные шаги |
| **[Executing Plans](./development-process/executing-plans.md)** | Выполняешь план с checkpoint'ами между задачами |
| **[Subagent Development](./development-process/subagent-driven-development.md)** | Параллельная работа над независимыми задачами через субагентов |
| **[Dispatching Agents](./development-process/dispatching-parallel-agents.md)** | Нужно запустить несколько агентов параллельно |
| **[Test-Driven Development](./development-process/test-driven-development.md)** | Пишешь код по методологии RED-GREEN-REFACTOR |
| **[Systematic Debugging](./development-process/systematic-debugging.md)** | Ищешь причину бага — 4-фазный процесс |
| **[Verification](./development-process/verification-before-completion.md)** | Проверка что всё работает перед заявлением "готово" |
| **[Finishing Branch](./development-process/finishing-a-development-branch.md)** | Завершаешь работу над веткой — merge, PR, cleanup |
| **[Git Worktrees](./development-process/using-git-worktrees.md)** | Нужна изолированная рабочая область |
| **[Feature Forge](./development-process/feature-forge.md)** | End-to-end реализация фичи |
| **[Spec Miner](./development-process/spec-miner.md)** | Извлечение требований из документации |
| **[The Fool](./development-process/the-fool.md)** | Нужен свежий взгляд, проверка assumptions |
| **[Doc Co-Authoring](./development-process/doc-coauthoring.md)** | Совместное написание документации |

### ✅ Code Quality & Review (10 скиллов)

Скиллы для повышения качества кода и эффективного code review.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Make No Mistakes](./code-quality/make-no-mistakes.md)** | Нужна максимальная точность — проверка перед каждым ответом |
| **[Code Reviewer](./code-quality/code-reviewer.md)** | Проводишь комплексный code review |
| **[Code Documenter](./code-quality/code-documenter.md)** | Нужно задокументировать код |
| **[Requesting Review](./code-quality/requesting-code-review.md)** | Запрашиваешь review своего кода |
| **[Receiving Review](./code-quality/receiving-code-review.md)** | Получил feedback и нужно правильно его обработать |
| **[Test Master](./code-quality/test-master.md)** | Разрабатываешь стратегию тестирования |
| **[Property-Based Testing](./code-quality/property-based-testing.md)** | Нужно генеративное тестирование свойств |
| **[Testing Handbook](./code-quality/testing-handbook-skills.md)** | Best practices тестирования |
| **[Differential Review](./code-quality/differential-review.md)** | Security-focused review diff'ов |
| **[Second Opinion](./code-quality/second-opinion.md)** | Нужен альтернативный взгляд на решение |

### 🔒 Security (10 скиллов)

Скиллы для security-аудита, поиска уязвимостей и безопасной разработки.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Semgrep Scan](./security/semgrep-security-scan.md)** | Запускаешь статический анализ кода |
| **[Security Reviewer](./security/security-reviewer.md)** | Security-focused code review |
| **[Secure Code Guardian](./security/secure-code-guardian.md)** | Пишешь код с учётом безопасности |
| **[Fullstack Guardian](./security/fullstack-guardian.md)** | Full-stack security review |
| **[Audit Context](./security/audit-context-building.md)** | Готовишь контекст для security audit |
| **[Sharp Edges](./security/sharp-edges.md)** | Ищешь опасные паттерны в коде |
| **[Insecure Defaults](./security/insecure-defaults.md)** | Проверяешь настройки по умолчанию |
| **[Variant Analysis](./security/variant-analysis.md)** | Нашёл уязвимость — ищешь похожие |
| **[Semgrep Rule Creator](./security/semgrep-rule-creator.md)** | Создаёшь кастомные правила Semgrep |
| **[Firebase APK Scanner](./security/firebase-apk-scanner.md)** | Сканируешь Android APK на Firebase уязвимости |

### 🔌 API & Backend (6 скиллов)

Скиллы для проектирования API и backend-разработки.

| Скилл | Когда использовать |
|-------|-------------------|
| **[API Designer](./api-backend/api-designer.md)** | Проектируешь REST/GraphQL API, OpenAPI спеки |
| **[Architecture Designer](./api-backend/architecture-designer.md)** | Проектируешь архитектуру системы |
| **[Microservices Architect](./api-backend/microservices-architect.md)** | Проектируешь микросервисную архитектуру |
| **[FastAPI Expert](./api-backend/fastapi-expert.md)** | Работаешь с FastAPI |
| **[NestJS Expert](./api-backend/nestjs-expert.md)** | Работаешь с NestJS |
| **[WebSocket Engineer](./api-backend/websocket-engineer.md)** | Реализуешь real-time функциональность |

### 🎨 Frontend (4 скилла)

Скиллы для frontend-разработки.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Frontend Design](./frontend/frontend-design.md)** | Создаёшь distinctive UI без "AI slop" |
| **[React Expert](./frontend/react-expert.md)** | Работаешь с React |
| **[Next.js Developer](./frontend/nextjs-developer.md)** | Работаешь с Next.js |
| **[React Native Expert](./frontend/react-native-expert.md)** | Разрабатываешь мобильное приложение на React Native |

### ☁️ Infrastructure & DevOps (7 скиллов)

Скиллы для инфраструктуры, CI/CD и DevOps.

| Скилл | Когда использовать |
|-------|-------------------|
| **[DevOps Engineer](./infrastructure/devops-engineer.md)** | Настраиваешь CI/CD, автоматизацию |
| **[Cloud Architect](./infrastructure/cloud-architect.md)** | Проектируешь облачную инфраструктуру |
| **[Kubernetes Specialist](./infrastructure/kubernetes-specialist.md)** | Работаешь с Kubernetes |
| **[Terraform Engineer](./infrastructure/terraform-engineer.md)** | Infrastructure as Code |
| **[Monitoring Expert](./infrastructure/monitoring-expert.md)** | Настраиваешь мониторинг, алерты, метрики |
| **[DevContainer Setup](./infrastructure/devcontainer-setup.md)** | Настраиваешь VS Code devcontainers |
| **[Git Cleanup](./infrastructure/git-cleanup.md)** | Чистишь git репозиторий |

### 🗄️ Database (3 скилла)

Скиллы для работы с базами данных.

| Скилл | Когда использовать |
|-------|-------------------|
| **[PostgreSQL Pro](./database/postgres-pro.md)** | Оптимизируешь PostgreSQL |
| **[Database Optimizer](./database/database-optimizer.md)** | Оптимизируешь запросы |
| **[SQL Pro](./database/sql-pro.md)** | Пишешь сложные SQL запросы |

### 💻 Languages (5 скиллов)

Скиллы для конкретных языков программирования.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Python Pro](./languages/python-pro.md)** | Пишешь идиоматичный Python |
| **[TypeScript Pro](./languages/typescript-pro.md)** | Пишешь качественный TypeScript |
| **[Go Pro](./languages/golang-pro.md)** | Пишешь идиоматичный Go |
| **[Swift Expert](./languages/swift-expert.md)** | Разрабатываешь на Swift/iOS |
| **[Modern Python](./languages/modern-python.md)** | Используешь фичи Python 3.10+ |

### 🤖 AI & Data (3 скилла)

Скиллы для работы с AI и данными.

| Скилл | Когда использовать |
|-------|-------------------|
| **[RAG Architect](./ai-data/rag-architect.md)** | Проектируешь RAG систему |
| **[Prompt Engineer](./ai-data/prompt-engineer.md)** | Оптимизируешь промпты для LLM |
| **[Pandas Pro](./ai-data/pandas-pro.md)** | Работаешь с данными в pandas |

### 🎨 Design & Creative (4 скилла)

Скиллы для дизайна и креативных задач.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Algorithmic Art](./design-creative/algorithmic-art.md)** | Создаёшь generative art на p5.js |
| **[Canvas Design](./design-creative/canvas-design.md)** | Создаёшь постеры, artwork в PNG/PDF |
| **[GIF Creator](./design-creative/gif-creator.md)** | Создаёшь анимированные GIF |
| **[Theme Factory](./design-creative/theme-factory.md)** | Создаёшь темы для презентаций |

### 📄 Documents & Office (4 скилла)

Скиллы для работы с офисными документами.

| Скилл | Когда использовать |
|-------|-------------------|
| **[DOCX](./documents/docx.md)** | Создаёшь/редактируешь Word документы |
| **[PDF](./documents/pdf.md)** | Работаешь с PDF файлами |
| **[PPTX](./documents/pptx.md)** | Создаёшь презентации PowerPoint |
| **[XLSX](./documents/xlsx.md)** | Работаешь с Excel файлами |

### 🧪 Testing & Automation (3 скилла)

Скиллы для тестирования и автоматизации.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Webapp Testing](./testing-automation/webapp-testing.md)** | Тестируешь веб-приложение |
| **[Playwright Automation](./testing-automation/playwright-automation.md)** | Автоматизируешь браузер |
| **[iOS Simulator](./testing-automation/ios-simulator.md)** | Автоматизируешь iOS симулятор |

### 🔧 Tools & CLI (3 скилла)

Скиллы для работы с инструментами и CLI.

| Скилл | Когда использовать |
|-------|-------------------|
| **[CLI Developer](./tools-cli/cli-developer.md)** | Разрабатываешь CLI инструмент |
| **[GH CLI](./tools-cli/gh-cli.md)** | Работаешь с GitHub CLI |
| **[Web Artifacts Builder](./tools-cli/web-artifacts-builder.md)** | Создаёшь React/Tailwind artifacts для Claude |

### 🔮 Meta / Skill Creation (5 скиллов)

Скиллы для создания новых скиллов и meta-задач.

| Скилл | Когда использовать |
|-------|-------------------|
| **[Skill Creator](./meta/skill-creator.md)** | Создаёшь новый скилл |
| **[MCP Builder](./meta/mcp-builder.md)** | Создаёшь MCP сервер |
| **[Writing Skills](./meta/writing-skills.md)** | TDD подход к написанию скиллов |
| **[Workflow Skill Design](./meta/workflow-skill-design.md)** | Проектируешь workflow скилл |
| **[Ask Questions](./meta/ask-questions-if-underspecified.md)** | Когда задавать уточняющие вопросы |

---

## 🏗️ Структура репозитория

```
skills/
├── README.md               # Этот файл
├── INDEX.md                # Детальный каталог
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

## 🤝 Contributing

1. Fork репозитория
2. Создай скилл в соответствующей категории
3. Добавь frontmatter:
```yaml
---
name: skill-name
description: "Когда использовать этот скилл"
---
```
4. Обнови INDEX.md
5. Создай PR

---

## 📜 Лицензия

Скиллы собраны из открытых репозиториев. Каждый скилл сохраняет лицензию оригинального источника.

---

## ⭐ Star History

Если библиотека полезна — поставь звезду!

---

**Создано с ❤️ для сообщества разработчиков**
