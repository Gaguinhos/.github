# Contributing to Gaguinhos

Welcome to **Gaguinhos**! We are thrilled that you’d like to contribute. Since this organization acts as a learning hub for students and developers, we take our code quality, pipelines, and processes seriously.

Please review the following guidelines before you open a pull request.

## 1. The "Main is Lava" Rule
Never push directly to the `main` branch. This is the golden rule.
- Always create a new branch for your work.
- Use explicit, conventional prefixes for branches so others know exactly what you are doing.

### Approved Branch Prefixes
- `feat/` — New features, components, or major behavior changes.
- `fix/` — Bug fixes.
- `chore/` — Maintenance, tooling updates, dependabot changes.
- `docs/` — Documentation improvements (README, etc.).
- `test/` — Adding or updating tests.
- `refactor/` — Rewriting existing code without changing its functionality.

## 2. Pull Request Process
1. Push your branch and open a Pull Request against the `main` branch.
2. The PR will automatically trigger the **Gaguinhos Universal Polyglot CI**.
3. **You must wait for the CI to pass.**
4. A minimum of one review from another Gaguinho is required.
5. Once approved and green, squash and merge your PR into `main`.

## 3. The Gaguinhos Universal CI
To ensure consistency across the whole organization without duplicating code snippet, we rely on a single, global CI workflow. 

To enable it on your repository, add the following to `.github/workflows/ci.yml`:

```yaml
name: Gaguinhos CI
on:
  pull_request:
    branches: [main]

jobs:
  call-polyglot-workflow:
    uses: Gaguinhos/.github/.github/workflows/master-ci.yml@main
```

The CI will automatically locate your language/framework and run the corresponding linter and tests. If your tests fail, fix them before demanding a review.

## 4. Local Development
Before opening a PR, ask yourself:
- Did I remove my debugging statements (`console.log`, `print`)?
- Did I verify there are no exposed secrets (API keys, passwords)?
- Do the tests pass locally?

If the answer is yes, we are excited to review your PR!