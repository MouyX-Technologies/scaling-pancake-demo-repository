README.md

MouyX Technologies Lab

«AI-powered software engineering, algorithmic trading, automation, and cloud infrastructure.»

Overview

MouyX Technologies Lab is a development and research environment focused on building reliable software systems with AI-assisted development, algorithmic trading, automation, DevOps, and cloud infrastructure.

The project is designed to work across:

- VS Code
- Cursor
- GitHub
- Gemini
- Firebase Studio
- Jules
- Python
- Node.js / TypeScript
- MQL4 / MQL5
- MetaTrader 5
- Docker
- Cloud infrastructure

Core Goals

1. Build production-ready software.
2. Automate repetitive engineering tasks.
3. Use AI agents for development, testing, documentation, and DevOps.
4. Maintain secure GitHub repositories and CI/CD pipelines.
5. Develop algorithmic-trading infrastructure.
6. Keep configuration, secrets, and deployment processes organized.
7. Document important architectural and operational decisions.

Repository Structure

project/
├── .github/
│   └── workflows/
│
├── .vscode/
│   ├── settings.json
│   ├── extensions.json
│   ├── launch.json
│   └── tasks.json
│
├── .cursor/
│   └── rules/
│
├── src/
├── tests/
├── scripts/
├── docs/
├── config/
├── deploy/
│
├── .editorconfig
├── .prettierrc.json
├── .prettierignore
├── eslint.config.js
├── package.json
├── package-lock.json
├── .env.example
├── .gitignore
└── README.md

Development Environment

VS Code

Use VS Code as the primary development environment.

Recommended extensions include:

- ESLint
- Prettier
- GitHub Pull Requests and Issues
- Docker
- Python
- MQL5
- GitLens
- YAML
- Markdown tooling

Cursor

Cursor can be used for AI-assisted coding, repository analysis, refactoring, testing, and documentation.

Project-specific Cursor rules should be stored in:

.cursor/rules/

Gemini

Gemini can be used as an additional AI development agent for:

- Code generation
- Code review
- Repository analysis
- Documentation
- Testing
- Architecture planning
- Firebase development

Jules

Jules can be used as an autonomous engineering agent for repository maintenance, issue resolution, testing, and GitHub workflows.

All automated changes should remain reviewable through Git history and pull requests.

Security

Never commit secrets to Git.

Do not commit:

.env
.env.*
*.pem
*.key
credentials.json
service-account*.json
secrets/

Use ".env.example" for documenting required environment variables.

Example:

API_KEY=
DATABASE_URL=
MT5_LOGIN=
MT5_PASSWORD=
MT5_SERVER=

Store production secrets in an appropriate secret-management system or GitHub Actions secrets.

Git Workflow

Recommended workflow:

main
 │
  ├── develop
   │
    ├── feature/*
     ├── fix/*
      ├── chore/*
       └── security/*

       Basic workflow:

       git pull
       git checkout -b feature/my-change

       # Make changes

       git add .
       git commit -m "feat: describe the change"
       git push -u origin feature/my-change

       Create a pull request before merging production changes.

       Quality Gates

       Before merging:

       npm install
       npm run lint
       npm test
       npm run build

       If the project contains Python:

       python -m pytest

       If Docker is used:

       docker build .

       Algorithmic Trading

       The trading infrastructure may support:

       - MetaTrader 5
       - MQL5 Expert Advisors
       - Python trading services
       - Market-data processing
       - Risk management
       - Signal generation
       - Backtesting
       - AI/ML models
       - Broker integrations
       - Trading dashboards

       Supported markets may include:

       XAUUSD
       BTCUSD
       EURUSD
       GBPUSD
       US100
       Stocks
       Indices
       Crypto
       Commodities

       Risk Management

       Trading software must enforce risk controls before sending orders.

       Example configuration:

       Risk per trade: 1%
       Maximum daily risk: 3%
       Maximum concurrent trades: 2
       Minimum risk/reward: 1.5:1
       Target risk/reward: 2:1
       ATR stop multiplier: 2.0

       These values are configuration examples and must be validated before live trading.

       AI Agent Architecture

       Agents should have clearly defined responsibilities.

       Example:

       Master / Orchestrator
       │
       ├── Coding Agent
       ├── Testing Agent
       ├── Security Agent
       ├── DevOps Agent
       ├── Documentation Agent
       ├── Trading Agent
       ├── Data Agent
       └── Review Agent

       Agents should:

       - Follow repository rules.
       - Never expose secrets.
       - Document important changes.
       - Run tests before reporting completion.
       - Avoid destructive operations without authorization.
       - Keep changes isolated and reviewable.

       CI/CD

       GitHub Actions should automate:

       Lint
        ↓
        Test
         ↓
         Build
          ↓
          Security Scan
           ↓
           Docker Build
            ↓
            Deploy

            Production deployments should require appropriate approvals and environment protection.

            Docker

            For services that require containers:

            docker compose up -d

            View logs:

            docker compose logs -f

            Stop services:

            docker compose down

            Documentation

            Important documentation belongs in:

            docs/

            Recommended documents:

            docs/
            ├── architecture.md
            ├── security.md
            ├── development.md
            ├── deployment.md
            ├── agents.md
            ├── trading.md
            └── troubleshooting.md

            Configuration

            Keep environment-specific configuration outside source code.

            Use:

            .env.example

            for required variable names and documentation.

            Never place real credentials in:

            - README files
            - Source code
            - Git commits
            - GitHub Issues
            - Pull requests
            - Public documentation
            - AI prompts

            Contribution Rules

            1. Keep changes focused.
            2. Follow existing project conventions.
            3. Add tests when appropriate.
            4. Run linting and tests before committing.
            5. Do not commit secrets.
            6. Update documentation when behavior changes.
            7. Use meaningful commit messages.
            8. Review AI-generated changes before production deployment.

            Commit Convention

            Recommended:

            feat: add new functionality
            fix: correct a bug
            docs: update documentation
            refactor: improve code structure
            test: add or update tests
            chore: maintenance
            security: security improvement
            ci: update CI/CD
            build: update build system

            Production Principle

            «Automate everything. Document everything. Secure everything.»

            Automation should improve reliability, not remove human accountability.

            AI agents may generate, modify, test, and review code, but production-critical changes must remain auditable.

            Status

            This repository is intended to evolve continuously as the MouyX Technologies Lab infrastructure develops.

            ---

            Maintainer: MouyX Technologies Lab
            Project Identity: Mouy-leng172
            Primary Focus: AI Engineering • Algorithmic Trading • Automation • DevOps • Cloud Infrastructure