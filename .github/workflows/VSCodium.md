VS Code Project Configuration

Repository

GitHub Repository: "MouyX-Technologies/scaling-pancake-demo-repository"

VS Code Configuration

The project uses a dedicated ".vscode/" directory for workspace configuration.

.vscode/
├── settings.json
├── extensions.json
├── launch.json
└── tasks.json

"settings.json"

Workspace settings should provide:

- Consistent formatting
- Automatic format-on-save
- ESLint integration
- Prettier integration
- Git configuration
- Clean editor behavior

Recommended configuration:

{
      "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode",
          "editor.codeActionsOnSave": {
                "source.fixAll.eslint": "explicit"
          },
            "eslint.validate": [
                    "javascript",
                        "javascriptreact",
                            "typescript",
                                "typescriptreact"
            ],
              "files.trimTrailingWhitespace": true,
                "files.insertFinalNewline": true,
                  "files.exclude": {
                        "node_modules": true,
                            ".git": true
                  }
}

"extensions.json"

Recommended extensions:

{
      "recommendations": [
            "esbenp.prettier-vscode",
                "dbaeumer.vscode-eslint",
                    "eamodio.gitlens",
                        "github.vscode-pull-request-github",
                            "ms-azuretools.vscode-docker",
                                "yzhang.markdown-all-in-one"
      ]
}

"launch.json"

Use "launch.json" for project debugging.

Example Node.js configuration:

{
      "version": "0.2.0",
        "configurations": [
                {
                          "type": "node",
                                "request": "launch",
                                      "name": "Launch Project",
                                            "program": "${workspaceFolder}/index.js",
                                                  "skipFiles": [
                                                            "<node_internals>/**"
                                                  ]
                }
        ]
}

Update the "program" path when the project entry point changes.

"tasks.json"

Use VS Code tasks for common development commands.

Example:

{
      "version": "2.0.0",
        "tasks": [
                {
                          "label": "npm: install",
                                "type": "npm",
                                      "script": "install",
                                            "problemMatcher": []
                },
                    {
                              "label": "npm: lint",
                                    "type": "npm",
                                          "script": "lint",
                                                "group": "build",
                                                      "problemMatcher": []
                    },
                        {
                                  "label": "npm: test",
                                        "type": "npm",
                                              "script": "test",
                                                    "group": "test",
                                                          "problemMatcher": []
                        },
                            {
                                      "label": "npm: build",
                                            "type": "npm",
                                                  "script": "build",
                                                        "group": "build",
                                                              "problemMatcher": []
                            }
        ]
}

Cursor Integration

Cursor uses:

.cursor/
└── rules/

Project-specific AI instructions should be stored inside ".cursor/rules/".

Recommended rules:

.cursor/rules/
├── project.mdc
├── coding-standards.mdc
├── security.mdc
└── git-workflow.mdc

Project Standards

The development environment follows:

Editor
  ↓
  Prettier
    ↓
    ESLint
      ↓
      Tests
        ↓
        Build
          ↓
          Git
            ↓
            GitHub

            Useful Commands

            Install dependencies:

            npm install

            Run development:

            npm run dev

            Run lint:

            npm run lint

            Run tests:

            npm test

            Build:

            npm run build

            GitHub Workflow

            git status
            git add .
            git commit -m "feat: update project"
            git push

            Before pushing production changes:

            npm run lint
            npm test
            npm run build

            Security

            Never commit:

            .env
            .env.local
            *.pem
            *.key
            credentials.json
            service-account.json

            Use environment variables or GitHub Secrets for sensitive configuration.

            Development Principle

            «Keep the repository clean, reproducible, secure, and AI-agent friendly.»

            VS Code, Cursor, GitHub, ESLint, and Prettier should work together as one consistent development environment.
                            }
                        }
                    }
                }
        ]
}
                                                  ]
                }
        ]
}
      ]
}
                  }
            ]
          }
}