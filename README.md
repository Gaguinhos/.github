# Gaguinhos `.github` Organization Settings

This repository contains the default community health files, issue/PR templates, and reusable GitHub Actions workflows for the **Gaguinhos** organization.

> 📝 **Note:** The documentation you see on the public Gaguinhos organization page is driven by `profile/README.md`. This current `README.md` is strictly for developers contributing to this repository itself.

## 🗂️ What's inside this repository?

```text
├── .github/                   # Reusable configurations
│   ├── ISSUE_TEMPLATE/        # Standardized issue forms (.yml)
│   └── workflows/             # Reusable central workflows
│       └── master-ci.yml      # The Universal Polyglot CI
├── PULL_REQUEST_TEMPLATE.md   # Organization-wide PR template
├── CODE_OF_CONDUCT.md         # Ethical and behavior standards
├── CONTRIBUTING.md            # "Main is Lava" and contribution rules
├── SECURITY.md                # Security vulnerability reporting policy
├── SUPPORT.md                 # How to get help
├── profile/
│   └── README.md              # Public face of the Gaguinhos GitHub Org
└── README.md                  # (This file)
```

## 🤖 The Universal Polyglot CI

The crown jewel of this repository is `.github/workflows/master-ci.yml`. It is a reusable workflow designed to run on any Gaguinhos repository. It automatically detects the language/framework (Node.js, Python, Terraform, Go, Rust, etc.) and executes the appropriate linting and testing commands.

### How to use the Universal CI in other repos

In the repository you want to enable tests for, create a file at `.github/workflows/ci.yml`:

```yaml
name: Super CI Check

on:
  pull_request:
    branches: [ "main" ]

jobs:
  run-master-ci:
    name: Call Polyglot Workflow
    uses: Gaguinhos/.github/.github/workflows/master-ci.yml@main
```

### Extending the CI

To add support for a new language, modify `.github/workflows/master-ci.yml`. Ensure you follow the structure of existing conditionally executed bash sections.

## 🤝 Adding Community Files

Any markdown file added to the root of this repository (`SECURITY.md`, `CODE_OF_CONDUCT.md`, `CONTRIBUTING.md`) acts as the default fallback for all repositories in the Gaguinhos organization.

## Contributing to these rules

Follow our own `CONTRIBUTING.md` when proposing changes to this repository. Do not push to `main`!