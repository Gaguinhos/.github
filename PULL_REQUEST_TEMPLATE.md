## PR Checklist

Before requesting a review, please confirm the following:

### 📝 Description
### 🤖 The Super CI Status
- [ ] **The CI is Green:** I have waited for the "Universal Polyglot CI" to finish and it passed successfully.
- [ ] **Stack Detection:** I verified in the CI logs that it correctly detected my tech stack (e.g., Node.js, Python, Terraform).
- [ ] **Linter Check:** I checked the Super-Linter output and fixed any major style or syntax warnings.

### ✅ The Gaguinhos Honor System
- [ ] I created a feature branch (e.g., `feat/`, `fix/`) and did not push to `main`.
- [ ] I have moved my card on the Project Board to "Testing".

### 🔒 Security & Secrets
- [ ] I verified that no `.env` files, API keys, or hardcoded passwords are in this PR.
- [ ] The **Gitleaks** CI check passed (no leaked secrets detected).
- [ ] I am not exposing any internal Gaguinhos server IPs or credentials.

### 🛠️ Code Quality
- [ ] I have tested this code locally and it works as expected.
- [ ] I removed all `console.log()`, `print()`, or debug statements.
- [ ] (If applicable) I ran `terraform fmt` and `terraform validate` locally.

### 🤝 Review Request
- [ ] I have tagged at least one Gaguinho to review this.
- [ ] I am ready to fix any feedback provided.
